<template>
 <div class="head" >
<div class="one"  v-for= "(item,index) in arr" :key="index">
<div>{{item.name}}&nbsp;&nbsp;&nbsp;{{item.tags[0].name}}&nbsp;&nbsp;&nbsp;{{item.tags[1].name}}</div>
<div class="two" >
<div class="three " v-for="(item1,index1) in item.tags" :key="index1">
<p>{{item1.name+"|"}}</p> 

</div>
<div class="three " v-for="(item2,index2) in item.recommend_courses" :key='index2'>

<p>{{item2.name+"|"}}<br></p>
</div>

</div>
</div>

<div class="q2"> <span>经营专区</span></div>
<div class="top">
 <swiper ref="mySwiper" :options="swiperOptions">
    <swiper-slide v-for="(item,index) in arr1" :key="index">
    <img :src="item.picture_url">
    </swiper-slide>
 
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</div>

 </div>
</template>

<script>
import { Swiper, SwiperSlide} from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'
import axios from "axios";
 export default {
   name: '',
   props: {
   },
   components: {
Swiper,
 SwiperSlide
   },
   data () {
     return {
       swiperOptions: {
          pagination: {
            el: '.swiper-pagination'
          },
          // Some Swiper option/callback...
        },
arr:[],
arr1:[]

     }
   },
   methods: {
getDate(){
  axios.get("http://120.78.14.107/api/v2/index/categories").then(res =>{
    
this.arr=res.data;

console.log(res.data)
     
  }).catch(err =>{
    console.log(err)
  })
},
 getData(){
    axios.get("http://120.78.14.107/api/v2/index/banner-pictures").then(res =>{
    
this.arr1=res.data;

console.log(res.data)
     
  }).catch(err =>{
    console.log(err)
  })
 }







   },
   mounted() {
this.getDate()
this.getDate1()
   },
   watch: {

   },
   computed: {

   }
 }
</script>

<style scoped lang='scss'>
.head{
    width: 1550px;
    height: 515px;
 
    position: relative;
    background: #e0a72d;
}

.one{
    line-height: 55px;
    width: 248px;
 height: 55px;
   border-bottom: 1px solid white;
    margin-left: 200px;
   color: white;

}
span{
  width: 120px;
 margin-left: 75px;
  line-height: 55px;
  border-radius:20px;
 background: red;
 color: white;
 border: 1px solid white;
}
.q2{
   margin-left: 200px;
      width: 248px;
 height: 55px;
  
}

.one:hover{
color: black;
background: white;
}


.q2:hover span{
  background: white;
  color: black;
}

.lunbo{
width: 900px;
height: 513px;
border: 1px solid black;
position: absolute;
left: 448px;
top: 0;
}

.two{
 
  position: absolute;
 left: 448px;
  top: 0;
  height: 400px;
  width: 350px;
  
}
  .three{
display: none;
p{
  float: left;
}

  }
  .one:hover  .three{
    display: block;
  }
  .two{
    display: none;
  }
  .one:hover .two{
    background: white;
    display: block;
  }

.top{
width:900px ;
height: 513px;
border: 1px solid black;
top: 0;
left: 448px;
position: absolute;

}

</style>
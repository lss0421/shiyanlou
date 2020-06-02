<template>
 <div class="h">
<div class="h1"><span class="c1">楼+实战课程|</span>定期开班,导师助教全程辅导,最快最优成长<span class="c2">更多></span></div>
<div class="h2" v-for="(item,index) in arr.slice(0,4)" :key="index">
<img :src="item.picture_url" alt="" class="h3">
<p class="h4">{{item.title}}</p>
<div class="h5">最近班次：{{item.open_time}}</div>
</div>
 </div>
</template>

<script>
import axios from 'axios';
 export default {
   name: '',
   props: {
   },
   components: {

   },
   data () {
     return {
arr:[]
     }
   },
   methods: {
getData(){
    axios.get('http://120.78.14.107/api/v2/index/louplus').then(res =>{
        this.arr=res.data
        console.log(data)
    }).catch(err =>{
        console.log(err)
    })
}
   },
   mounted() {
this.getData()
   },
   watch: {

   },
   computed: {

   }
 }
</script>

<style scoped lang='scss'>

.h1{
    width: 1155px;
    height: 95px;
    
    margin: auto;
    line-height: 95px;
    position: relative;
}
.c1{
    font-size: 20px;
    font-weight: 700;
}
.c2{
    position: absolute;
    right: 10px;
}
.h{
    height: 305px;
}
.h2{
    
    width: 270px;
    height: 180px;
    position: relative;
   float: left;
   margin-left: 100px;
   border-radius:  15px 15px;
 
}
.h2:hover{
    box-shadow: 10px -10px 5px #888888;
}

.h3{
    width: 270px;
    height: 90px;
    position: absolute;
}
.h4{
    width: 270px;
    height: 45px;
    text-align: center;
    line-height: 45px;
    position: absolute;
    top: 90px;
    font-size: 20px;
}
.h5{
     width: 270px;
    height: 45px;
    text-align: center;
    line-height: 45px;
    position: absolute;
    top: 135px;
    color: gray;
}


</style>

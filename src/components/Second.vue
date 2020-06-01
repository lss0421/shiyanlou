<template>
 <div class="head">
<div class="one"  v-for= "(item,index) in arr" :key="index">
<div class="q1">{{item.name}}</div>
</div>

<div class="q2"> <span>经营专区</span></div>
 </div>
</template>

<script>
import axios from "axios";
 export default {
   name: '',
   props: {
   },
   components: {

   },
   data () {
     return {
arr:[],
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
}



   },
   mounted() {
this.getDate()
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
    border: 1px solid blue;
}

.one{
    line-height: 55px;
    width: 248px;
 height: 55px;
    border: 1px solid black;
    margin-left: 200px;
   color: white;

}
span{
  width: 100px;
 margin-left: 75px;
  line-height: 55px;
  border-radius:25px;
 background: red;
 color: white;
 
}
.q2{
   margin-left: 200px;
      width: 248px;
 height: 55px;
  border: 1px solid black;
}
.q3{

}
</style>
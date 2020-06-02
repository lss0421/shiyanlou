<template>
 <div>

<div class="d1" v-for="(item,index) in arr.slice(0,1)" :key="index">
<!-- {{item.classify_name+"|"}}{{item.description}}
<img :src="item.picture_url"> -->
</div>
<div class="d2" v-for="(item,index) in arr.slice(1)" :key="index">

</div>

 </div>
</template>

<script>
import axios from 'axios'
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
    axios.get().then(res =>{
this.arr=res.data
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
.d1{
    width: 560px;
    height: 330px;
    border: 1px solid black;
}
.d2{
    width: 260px;
    height: 250px;
    border: 1px solid black;
}
</style>

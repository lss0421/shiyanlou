<template>
 <div class="head">
<div class="bt1">
<div class="a1"> <img src="../assets/logo.png"></div>
<div class="a2">做实验,学编程</div>
<div class="a3">企业版|学校版</div>
<div class="a4">登陆</div>
<div class="a5"><span>注册</span></div>
</div>

<div class="bt2">
<div class="b1"><img src="../assets/quanbu.png"></div>
<div class="b2">路径</div>
<div class="b3">训练营</div>
<div class="b4">楼＋</div>
<div class="b5">会员<img data-v-ac00dc36="" src="https://static.shiyanlou.com/frontend/dist/img/02a4001.svg"></div>
<div class="b6">社区<img src="../assets/三角.jpg" style="width:15px;height:15px;">
<div class="tb" id="w1">讨论</div>
<div class="tb" id="w2">教程库</div>
<div class="tb" id="w3">直播</div>
<div class="tb" id='w4'>比赛</div>


</div>
<div class="b7"><input type="text" placeholder="搜索 课程/问答" ><img src="../assets/搜索.jpg" style="width:15px;height:15px;"></div>
</div>









 </div>
</template>

<script>
 export default {
   name: '',
   props: {
   },
   components: {

   },
   data () {
     return {

     }
   },
   methods: {

   },
   mounted() {

   },
   watch: {

   },
   computed: {

   }
 }
</script>

<style scoped lang='scss'>
*{
    margin: 0;
    padding: 0;
}
.head{
   width: 1550px; 
   height: 155px;
   
   position: relative;
   background: #F9F9F9;
}
.head{
    div{
        div:hover{
cursor: pointer;
        }
    }
}
.bt1 .bt2{
    position: relative;
}



.a1{
    margin-left: 210px;
    margin-top: 25px;
    float: left;
    
}

.a2{
    float: left;
margin-right: 15px;
margin-top: 40px;
font-size: 18px;
}

.a3{
    float: left;
    margin-left:600px;
margin-top: 40px;
color: #08BF91;
}
.a4{
    position: absolute;
    right: 350px;
   top: 40px;
   color: #08BF91;
}

.a5{
    width:80px ;
    height: 47px;
    background-color:#08BF91;
    position: absolute;
right: 250px;
top: 25px;
text-align: center;

}
span{
    margin: auto;
    line-height: 47px;
    color: white;
}
 .b1{
     position: absolute;
     left: 200px;
    top: 91px;
 }

.b2{
    width: 75px;
    height: 63px;
   background-color: white;
    position: absolute;
        left: 450px;
    top: 92px;
    text-align: center;
    line-height: 63px;
}
.b3{
    width: 75px;
    height: 63px;
   background-color: white;
    position: absolute;
        left: 525px;
    top: 92px;
    text-align: center;
    line-height: 63px;
}

.b4{
    width: 75px;
    height: 63px;
    background-color: white;
    position: absolute;
        left: 600px;
    top: 92px;
    text-align: center;
    line-height: 63px;
}

.b5{
    width: 75px;
    height: 63px;
    background-color: white;
    position: absolute;
        left: 675px;
    top: 92px;
    text-align: center;
    line-height: 63px;
}

.b6{
    width: 75px;
    height: 63px;
   background-color: white;
    position: absolute;
        left: 750px;
    top: 92px;
    text-align: center;
    line-height: 63px;
}

.b7{
    position: absolute;
        right:  300px;
    bottom: 40px;
    
}
.b2:hover{
color:#08BF91; 
}
.b3:hover{
color:#08BF91; 
}
.b4:hover{
color:#08BF91; 
}
.b5:hover{
color:#08BF91; 
}
.b6:hover{
color:#08BF91; 
}
 .b7>input{
     border-radius: 16px!important;
 }
  .tb{
      width: 150px;
      height:50px ;
      display: none;
      background-color: white;
      color: black;
      line-height: 50px;
      text-align: center;
  }
  .b6:hover .tb{
      
      display: block;
  }
#w1:hover{
background: #F7F7F7;
}
#w2:hover{
background: #F7F7F7;
}
#w3:hover{
background: #F7F7F7;
}
#w4:hover{
background: #F7F7F7;
}
</style>
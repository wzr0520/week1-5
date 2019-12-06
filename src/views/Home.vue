<template>
  <div class="home-page">
<el-carousel height="150px">
    <el-carousel-item v-for="item in list" :key="item.id">
     <img :src="item.pic" alt="">
    </el-carousel-item>
</el-carousel>
      
    <div class="list">
      <div class="list-item" v-for="item in list" :key="item.id">
        <img :src="item.pic" alt />
        <p>{{item.name}}</p>
      </div>
    </div>
    <NavTab></NavTab>
  </div>
</template>

<script>
import NavTab from "../components/NavTab";
import datas  from "../data";

export default {
  name: "home",
  data(){
return{
    list:datas.list
}
  },
  components: {
    NavTab
  }
};
</script>

<style lang="scss">
.list{
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    border-bottom: 1px solid #ccc;
    padding-bottom: 10px;
    margin-top: 20px;
}
.list-item{
    width: 25%;
    height: 100px;
    margin-top: 10px;
img{
width:90%;
margin-left: 5%;
height:75px;
border-radius: 50%;
}
p{
    width: 100%;
    height: 25px;
    line-height: 25px;
    text-align: center
}
}
.el-carousel{
    width: 375px;
}
.el-carousel__container{
      width: 375px;
}
.el-carousel_item{
    width: 375px;
    height: 150px;
}
.el-carousel_item img{
    width: 375px;
    height: 150px;
    margin: 0;
    
}

</style>

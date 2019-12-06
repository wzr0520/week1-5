<template>
  <div class="nav-tab">
      <router-link to="/home">首页</router-link>
      <router-link to="/my">我的</router-link>

  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.nav-tab{

    display: flex;
    justify-content: space-around;
    width: 100%;
    height: 40px;
    line-height: 40px;
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    background: #eee;
    a{
        color: #000;
        text-decoration: none
    }
    .router-link-active{
        color: orangered
    }
}
</style>
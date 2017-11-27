<template>
  <div id="app">
  <div class="header__wrapper">
    <my-header class="container"></my-header>
  </div>
  <div class="main__wrapper container">
    <my-aside></my-aside>
    <my-main></my-main>
  </div>
  <my-footer></my-footer>
   <!--  <router-view/> -->
  </div>
</template>
<script>
import iconfont from '@/assets/iconfont.js'
import myHeader from '@/components/header'
import myAside from '@/components/aside'
import myMain from '@/components/main'
import myFooter from '@/components/footer'
export default {
  name: 'app',
  components: {
    myHeader,
    myAside,
    myMain,
    myFooter,
  },
  // props: ['mainColor']
}
</script>

<style lang="scss">
  html {
    font-size: 62.5%;  //10 ÷ 16 × 100% = 62.5%
  }
  body{
    font-size:1.6em;
    background-color:#e0e0e0;
  }
  ul{
    list-style:none;
  }
  dd{
    margin-left:1rem;
  }
  a{
    text-decoration: none;
    display: block;
  }
  .icon {
   width: 1.2em; height: 1.2em;
   vertical-align: -0.15em;
   fill: currentColor;
   overflow: hidden;
  }
  .header__wrapper{
    background-color:#fff;
  }
  .main__wrapper{
    position:relative;
    border-radius:0.4em;
    .aside{
      top:0;
      bottom:0;
      box-sizing:border-box;
    }
  }
    .container{
      width:100%;
    }
    .main__wrapper{
      margin-top:0;
      .aside{
        position:relative;
        width:100%;
      }
      .main{
        left:0;
        width:100%;
      }
    }

  .header .menu {
    float: none!important;
    margin-top:6rem;
  }
  .el-menu--horizontal .el-menu-item {
    float: none!important;
  }

  @media screen and (min-width:768px) {
  .header{
    button{
      display:none;
    }
    .el-menu{
      display:block;
    }
  }
  .container{
    margin:0 auto;
    width:104rem;
  }
  .main__wrapper{
    margin-top:1rem;
    .aside{
      position:absolute;
      width:30rem;
    }
    .main{
      position:relative;
      left:30rem;
      width:74rem;
    }
  }
  .header .menu {
    float: right!important;
    margin-top:0;
  }
  .el-menu--horizontal .el-menu-item {
    float: left!important;
  }
}
</style>

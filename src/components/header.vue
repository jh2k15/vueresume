<template>
  <div class="header">
    <h1>
      <a href=""><img src="../assets/jh2k15.png" height="40" alt=""></a>
    </h1>
      <button @click="isActive =!isActive ">
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>

        <el-menu :default-active="activeIndex" :class="{'errorClass': isActive }" class="menu" mode="horizontal" @select="handleSelect">
          <el-menu-item index="1">web</el-menu-item>
          <el-menu-item index="2"><a href="#">转word</a></el-menu-item>
          <el-menu-item index="3"><a href="#">转PDF</a></el-menu-item>
          <el-menu-item index="4"><el-color-picker v-model="mainColor"></el-color-picker></el-menu-item>
        </el-menu>

  </div>
</template>

<script>
export default {
  name:'header',
  data() {
    return {
      isActive :true,
      activeIndex: '1',
      mainColor:'#409eff',
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}

</script>

<style lang='scss'>
.errorClass{
  display:none;
}
  .header{
    position:relative;
    overflow:hidden;
    h1{
      line-height:6rem;
      margin: 0;
      padding-left:20px;
      float:left;
      img{
        vertical-align: sub;
      }
    }
    .menu{
      float:right;
    }
  button{
    box-sizing:border-box;
    width:4rem;
    height:4rem;
    padding:.8rem;
    background-color: #fff;
    border:none;
    // border:.1rem solid #e6e6e6;
    position: absolute;
    margin-top:10px;
    right:2rem;
    cursor:pointer;
    .icon-bar{
      background-color: #888;
      display: block;
      width: 2.2rem;
      height: .2rem;
      border-radius: .1rem;
    }
    .icon-bar+.icon-bar{
      margin-top: .4rem;
    }
  }
    .fade-enter-active, .fade-leave-active {
    transition: opacity .5s
    }
    .fade-enter, .fade-leave-to{
      opacity: 0
    }
  }

</style>

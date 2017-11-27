<template>
  <div class="main">
    <ul>
      <li>
        <dt>
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-heart20"></use>
          </svg>
          Skill. 技能清单
        </dt>
        <ul class="skill">
          <li>能够用 HTML5/CSS3 编写语义化的代码，完成较复杂的布局，实现跨浏览器和平台的兼容性开发，熟悉Bootstrap框架以及，scss 等css预处理，后处理工具</li>
          <li>熟练使用JavaScript，jQuery实现所需动画效果及交互效果。了解Vue.js，Angular，react前端框架，有单页面应用开发经验</li>
          <li>有后端语言php，数据库Mysql基础，购买了阿里云ECS服务器部署网站，做过cms博客</li>
          <li>有一定的美学基础，具有良好的设计感与图片处理能力，原型设计能力</li>
          <li>具备视频制作，视频剪辑，视频特效处理能力</li>
        </ul>
      </li>
      <li>
        <dt>
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-heart20"></use>
          </svg>
          Experience. 个人项目与实习经验
        </dt>
        <h3>个人项目</h3>
        <ul class="exp">
          <li v-for="(item,index) in arr">
            <div class="circle"></div>
            <h4>{{item.title}}
              <a href="javascript:;"><svg class="icon" aria-hidden="true"><use xlink:href="#icon-iconfont"></use></svg>SourceCode</a></h4>
            <div><p>{{item.info}}</p></div>
          </li>
        </ul>
        <h3>实习项目</h3>
        <ul class="exp">
          <li v-for="(item,index) in arr2">
            <div class="circle"></div>
            <h4>{{item.title}}
              <a href="javascript:;"><svg class="icon" aria-hidden="true"><use xlink:href="#icon-iconfont"></use></svg> SourceCode</a></h4>
            <div><p>{{item.info}}</p></div>
          </li>
          <li>
            <div class="circle"></div>
            <h4>Resume 2017.11 <a href="javascript:;"><svg class="icon" aria-hidden="true"><use xlink:href="#icon-iconfont"></use></svg> SourceCode</a></h4>
            <div class="clearfix"><img src="../assets/QRcode.png" alt=""><p>一份抢手的简历，应用html+css排版出一份网页版简历。一开始是用word文档写了一篇简历，就得没有心意，就写了个网页版，也是发挥了自己的强项，也锻炼了自己对色彩协调，排版的把握，最近又修改了内容，重构了代码，让页面加载变快</p></div>
          </li>
        </ul>
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name:'main',
  data () {
    return {
      arr:[
        {
          title:'Blog 2017.3',
          info:'继实训教了cms框架之后，就有写个个人博客的想法，重构了之前实训的代码，换成bootstrap项目，基于bootstrap+ sass + dedecms 搭建的 前后端分离 +文章发布系统'
        },
        {
          title:'Website 2017.4',
          info:'四月最高兴的事情就是购买了一个阿里服务器，配置完，用pagefull.js写了个单页面作为网站主页，往服务器里放置了一些自己做过的网页，在手机上也能看真是爽'
        },
        {
          title:'learn-webpack 2017.8',
          info:'暑假跟着教程写了个多页面应用，数据模板分离的思想，webpack打包，开发过程中主要是研究了怎么配置webpack，怎么实时开发浏览结果，怎么安排项目结构，自动化编译'
        },
        {
          title:'vue-first 2017.10',
          info:'vue越来越火了，看了一下vue官方文档，写了一个单页面应用，双向数据绑定确实很有意思，组件化应用构建也很酷，遇到很对小问题，通过查文档，最终还是完成了'
        },
      ],
      arr2:[
        {
          title:'first-love 2016.6',
          info:'这是我接手的第一个项目，为了适应团队协作完成页面我快速学习了php，数据库mysql语法等等。然后在实践中巩固，最终一个周左右实现了这个项目的前端部分。第二周，用php将多个页面串联成一个完整网站，从此一发不收拾'
        },
        {
          title:'whole-web 2016.12',
          info:'接手这个项目时已经对团队的框架比较熟悉了，在这个项目中锻炼了页面编写能力，比如首页头部的滚动隐藏，规范了表单，Grid的布局，自定义表单控件，弹出层等等。一个人在两周内独立完成一个网站，确实不易，细节很多，也比较考验布局能力。我再对老师的需求做出修改，整个过程下来收获很多，是一次蜕变'
        },
        {
          title:'CMS 2017.3',
          info:'这个项目相当于一个博客系统，大量的数据，处理数据，渲染到前端页面上。套用模板语言，数据跟表单一一对应，学一门新的框架，既大大减少了代码量，也提高了灵活性，边写边学边测试'
        },
      ]
    }
  }

}
</script>

<style lang="scss">
  $color2:#00796B;
  .main{
    background-color: #fff;
    &>ul{
      margin: 0;
      padding:1.4rem 2rem;
      li{
        padding-top:2rem;
        .exp{
          padding-left:0;
          border-left:.2rem solid $color2;
          margin-left:1.5rem;
          li{
            position:relative;
            top:-0.5rem;
            margin:2rem 0 2rem 2rem;
            padding-top: 0;
            img{
              width:15rem;
              float:left;
              margin-right:1rem;
            }
            p{
              font-size:1.5rem;
              line-height:2.2rem;
              margin:0;
              color:#616161;
            }
          }
        }
      }
      dt{
        font-size:2.4rem;
        color:$color2;
        line-height:3rem;
        border-bottom:.1rem solid $color2;
        margin-bottom:1.5rem;
      }
      dd{
        line-height:2.2rem;
        font-size:1.5rem;
        color:#616161;
      }
    }
    .circle{
      width:1.4rem;
      height:1.4rem;
      border-radius:100%;
      background-color:$color2;
      // float:left;
      position:absolute;
      left:-2.8rem;
      &+h4{
        margin-bottom:1rem;
        font-size:1.8rem;
        line-height:2rem;
        color:#000;
        position:relative;
        top:-0.2rem;
        a{
          display:inline;
          color:$color2;
          font-size:1.1rem;
          font-weight:normal;
          padding:.1rem .2rem;
          border:.1rem solid $color2;
          border-radius:.5rem;
        }
      }
    }
  }
  .clearfix{
    overflow:hidden;
    zoom:1;
    &:before{
      content:"";
      display:table;
    }
    &:after{
      content:"";
      clear:both;
    }
  }
  .skill{
    list-style-type:circle;
      li{
        color:#616161;
      }
      li:first-child{
        padding-top:0;

      }
  }
  h3{
    font-size:2.2rem;
    color:$color2;
  }
</style>

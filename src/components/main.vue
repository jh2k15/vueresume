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
          <li>有后端语言php，数据库Mysql基础，购买了阿里云ECS服务器部署网站，做了cms博客</li>
          <li>有一定的美学基础，具有良好的设计感与图片处理能力，原型设计能力</li>
          <li>有视频制作，视频剪辑，特效处理能力</li>
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
              <a href="javascript:;">SourceCode</a></h4>
            <div><p>{{item.info}}</p></div>
          </li>
        </ul>
        <h3>实习项目</h3>
        <ul class="exp">
          <li v-for="(item,index) in arr2">
            <div class="circle"></div>
            <h4>{{item.title}}
              <a href="javascript:;">SourceCode</a></h4>
            <div><p>{{item.info}}</p></div>
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
          title:'my-blog 2017.3',
          info:'用来练手bootstrap的项目，基于bootstrap+ sass + dedecms 搭建的 前后端分离 +文章发布系统'
        },
        {
          title:'my-website 2017.4',
          info:'四月购买了一个服务器，配置完，用pagefull写了个单页面作为网站主页，服务器放置了一些自己的demo'
        },
        {
          title:'webpack 2017.8',
          info:'暑假自己写了个多页应用，数据模板分离的思想，webpack打包，开发过程中主要是研究了怎么配置webpack，怎么实时开发浏览结果，怎么安排项目结构，自动化编译。'
        },
        {
          title:'vue-first 2017.10',
          info:'看了一下vue官方文档，写了一个简单的单页面应用，双向数据绑定确实很有意思，组件化应用构建也很酷'
        },
      ],
      arr2:[
        {
          title:'Webpack-t',
          info:'企业老师实训，赵腾飞php工程师，王丹丹设计专业博士导师。这是我接手的第一个项目，为了适应团队协作完成页面我快速学习了php，数据库mysql语法等等。然后在实践中巩固，最终一个周左右实现了这个项目的前端部分。'
        },
        {
          title:'Webpack-t 2017.2',
          info:'企业老师实训，赵腾飞php工程师，雷军网站规划与开发技术博士导师。接手这个项目时已经对团队的框架比较熟悉了，在这个项目中锻炼了页面编写能力，比如首页头部的滚动隐藏，规范了表单，Grid的布局，自定义表单控件，弹出层等等。一个人在两周内独立完成一个网站，确实不易，细节很多，也比较考验布局能力。我再对老师的需求做出修改，整个过程下来收获很多，是一次蜕变。 '
        },
        {
          title:'Webpack-t 2017.2',
          info:'雷军网站规划与开发技术博士导师。这个项目相当于一个博客系统，大量的数据，处理数据，渲染到前端页面上。一开始我写了一堆php，数据跟表单一一对应，后来发现这样做代码量很大，而且不够灵活。后来重新安排数据结构，正在学一门新的框架，既大大减少了代码量，也提高了灵活性，边写边学边测试。'
        },
        {
          title:'resume 2017.11',
          info:'刘磊企业级高级导师，一份抢手的简历，应用html+css排版出一份网页版简历。一开始是用word文档写了一篇简历，就得没有心意，就写了个网页版，也是发挥了自己的强项，也锻炼了自己对色彩协调，排版的把握。重构代码'
        },
      ]
    }
  }

}
</script>

<style lang="scss">
  .main{
    background-color: #fff;
    &>ul{
      margin: 0;
      padding:1.4rem 2rem;
      li{
        padding-top:2rem;
        .exp{
          padding-left:0;
          border-left:.2rem solid #00796b;
          margin-left:1.5rem;
          li{
            position:relative;
            top:-0.5rem;
            margin:2rem 0 2rem 2rem;
            padding-top: 0;
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
        color:#00796b;
        line-height:3rem;
        border-bottom:.1rem solid #00796b;
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
      background-color:#00796b;
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
          color:#00796b;
          font-size:1rem;
          font-weight:normal;
          padding:.1rem .2rem;
          border:.1rem solid #00796b;
          border-radius:.5rem;
        }
      }
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
    color:#00796B;
  }
</style>

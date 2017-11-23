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
        <dd>主修课程：网页前端开发、图像处理、视频剪辑、视频特效制作、移动UI设计</dd>
        <dd>选修课程：</dd>
      </li>
      <li>
        <dt>
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-heart20"></use>
          </svg>
          Experience. 个人项目与实习经验
        </dt>
        <ul>
          <li v-for="(item,index) in arr">
            <div class="circle"></div>
            <h4>{{item.title}}</h4>
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
          title:'Webpack-t 2017.2',
          info:'寒假自己写了个多页应用脚手架，数据模板分离的思想，webpack打包，开发过程中主要是研究了怎么配置webpack，怎么实时开发浏览结果，怎么安排项目结构。'
        },
        {
          title:'Webpack-t 2017.2',
          info:'开发框架的过程中，自己写了个前端端架，已发布在GitHub上。用 sass编译器的特点，创建不同的文件名，达到易于管理。'
        },
        {
          title:'Webpack-t 2017.2',
          info:'四月购买了一个服务器，配置完，用pagefull写了个单页面作为网站主页，服务器还放置自己自学的一些demo http:www.jh2k15.online'
        },
        {
          title:'Webpack-t 2017.2',
          info:'用来练手bootstrap的项目，基于bootstrap+ sass + dedecms 搭建的 前后端分离 +文章发布系统 http:dede.jh2k15.online'
        },
        {
          title:'Webpack-t 2017.2',
          info:'用来练手bootstrap的项目，基于bootstrap+ sass + dedecms 搭建的 前后端分离 +文章发布系统 http:dede.jh2k15.online'
        },
        {
          title:'Webpack-t 2017.2',
          info:'用来练手bootstrap的项目，基于bootstrap+ sass + dedecms 搭建的 前后端分离 +文章发布系统 http:dede.jh2k15.online'
        },
        {
          title:'Webpack-t 2017.2',
          info:'用来练手bootstrap的项目，基于bootstrap+ sass + dedecms 搭建的 前后端分离 +文章发布系统 http:dede.jh2k15.online'
        },
        {
          title:'Webpack-t 2017.2',
          info:'用来练手bootstrap的项目，基于bootstrap+ sass + dedecms 搭建的 前后端分离 +文章发布系统 http:dede.jh2k15.online'
        },
        {
          title:'Webpack-t 2017.2',
          info:'用来练手bootstrap的项目，基于bootstrap+ sass + dedecms 搭建的 前后端分离 +文章发布系统 http:dede.jh2k15.online'
        },
        {
          title:'Webpack-t 2017.2',
          info:'用来练手bootstrap的项目，基于bootstrap+ sass + dedecms 搭建的 前后端分离 +文章发布系统 http:dede.jh2k15.online'
        },
        {
          title:'Webpack-t 2017.2',
          info:'用来练手bootstrap的项目，基于bootstrap+ sass + dedecms 搭建的 前后端分离 +文章发布系统 http:dede.jh2k15.online'
        },
        {
          title:'Webpack-t 2017.2',
          info:'用来练手bootstrap的项目，基于bootstrap+ sass + dedecms 搭建的 前后端分离 +文章发布系统 http:dede.jh2k15.online'
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
        ul{
          padding-left:0;
          border-left:.2rem solid #00796b;
          margin-left:1.5rem;
          li{
            position:relative;
            top:-0.5rem;
            margin:2rem 0 2rem 2rem;
            padding-top: 0;
            p{
              font-size:1.4rem;
              line-height:2.2rem;
              margin:0;
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
      }
    }
  }
</style>

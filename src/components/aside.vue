<template>
  <div class="aside">
      <h1><img src="../assets/jh2k15.jpg" height="180" alt=""></h1>
      <h2>一腔热血的激情</h2>
      <ul class="">
        <li v-for="(item,index) in arr">
          <dt>
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-heart20"></use>
            </svg>
            {{item.title}}
          </dt>
          <dd v-for="ite in item.data">
             {{ite}}
          </dd>
        </li>
        <li class="skill">
          <dt>
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-heart20"></use>
            </svg>
            Tech. 技能点
          </dt>
          <dd>
            <span>html</span>
            <el-progress :text-inside="true" :stroke-width="18" :percentage="20" status="success"></el-progress>
          </dd>
          <dd>
            <span>html</span>
            <el-progress :text-inside="true" :stroke-width="18" :percentage="20" status="success"></el-progress>
          </dd>
          <dd>
            <span>html</span>
            <el-progress :text-inside="true" :stroke-width="18" :percentage="20" status="success"></el-progress>
          </dd>
          <dd>
            <span>html</span>
            <el-progress :text-inside="true" :stroke-width="18" :percentage="20" status="success"></el-progress>
          </dd>
        </li>
      </ul>
  </div>
</template>

<script>
export default {
  name: 'aside',
  data () {
    return {
      arr:[
        {
          title:'Basic info. 基本信息',
          data:[
            '个人信息: 连佳豪 / 男 / 22岁 / 大三',
            '院校：深圳信息学院',
            '专业：网页前端开发',
            '爱好:魔方、篮球'
            ]
        },
        {
          title:'Contact. 联系方式',
          data:[
            '邮箱: 734055405@qq.com',
            '微信: jh2k15'
            ]
        },
        {
          title:'Application. 应聘岗位',
          data:[
            'Web前端实习生'
            ]
        },
        {
          title:'Certificate. 证书',
          data:[
            '大学英语四级',
            '网页设计师证',
            '年度奖学金'
            ]
        },
      ]
    }
  }

}

</script>

<style lang='scss'>
  .aside{
    background-color:#409EFF;
    padding:1.4rem;
    h1,h2{
      text-align:center;
      margin-top:2rem;
    }
    h2{
      margin-bottom:0;
    }
    ul{
      margin:0;
      padding:0;
      li{
        padding-top:2rem;
        dt{
          font-size:1.8rem;
          color:#9f3;
          line-height:4rem;
        }
        dd{
          font-size:1.4rem;
          color:#fff;
          line-height:2rem;
        }
      }
    }
  }
  .skill{
    dd{
      padding-bottom:0.3rem;
      &>div{
        display:inline-block;
        width:18rem;
      }
    }
  }
</style>

<template>
  <div class="index-page">
    <div class="header-div">
      <!-- 登陆注册 -->
      <div class="header-nav-div">
        <div class="login-warpper">
          <div class="handle-view">
            <div class="item">API接口</div>
            <div class="item">下载应用</div>
            <div class="item">帮助</div>
            <div class="item" style="color:#E12128">云平台登陆</div>
            <div class="item register">注册</div>
          </div>
        </div>
      </div>
      <!-- 登陆注册end -->

      <!-- 导航 -->
      <div class="nav-div">
        <div class="nav-div-warp">
          <div class="nav-div-warp-box">
            <div class="logo-div">
              <img src="../assets/images/logo.png" alt="" srcset="">
            </div>
            <div class="text-div">
              <div class="item">首页</div>
              <div class="item">解决方案</div>
              <div class="item">产品</div>
              <div class="item">客户案例</div>
              <div class="item">服务与支持</div>
              <div class="item">联系我们</div>
            </div>
          </div>
        </div>
      </div>
      <!-- 导航end -->


      <!-- banner -->
      <div class="banner-div">
        <div class="banner-div-warp">
          <div class="banner-div-warp__box">
            <div class="box-left">
              <div class="text">不破坏章体 支持章型 <span>98%</span></div>
              <div class="btn">了解详情</div>
            </div>
            <div class="box-right">
              <img src="../assets/images/印章.png" alt="" srcset="">
            </div>
          </div>
        </div>
      </div>
      <!-- banner end -->
     </div>

      <!-- 不破坏到非法预警 -->
      <div class="banner-bottom-div">
        <div class="banner-bottom-div-warp">
          <div class="banner-bottom-div-warp__box">
            <div class="item" v-for="item in option1" :key="item.text1">
              <div class="icon-div">
                <img :src="item.icon" alt="" srcset="">
              </div>
              <div class="text-1">{{item.text1}}</div>
              <div class="text-2">{{item.text2}}</div>
              <div class="text-3">{{item.text3}}</div>
            </div>
          </div>
        </div>
      </div>
      <!-- 不破坏到非法预警end -->

      <!-- 解决方案 -->
      <div class="solution-div">
        <div class="solution-div-warp">
          <div class="title-div">
            <div class="text-1">云网边端一体化解决方案  助力企业数字化转型</div>
            <div class="text-2">思格特智能印章机系统</div>
          </div>
          <div class="tabs-div-warp">
            <div :class="'tabs-div ' + activeName">
              <el-tabs v-model="activeName">
                <el-tab-pane label="本地私有一体化" name="first"><SolutionItem activeName="first"/></el-tab-pane>
                <el-tab-pane label="公私混托一体化" name="second"><SolutionItem activeName="second"/></el-tab-pane>
                <el-tab-pane label="云网边端一体化" name="third"><SolutionItem activeName="third"/></el-tab-pane>
              </el-tabs>
            </div>
          </div>
        </div>
      </div>
      <!-- 解决方案end -->
  </div>
</template>
<script>
let o = {
  first:{
    activeName:'本地私有一体化',
    activeImgSrc:require('../assets/images/sol1.png')
  },
  second:{
    activeName:'公私混托一体化',
    activeImgSrc:require('../assets/images/sol2.png')
  },
  third:{
    activeName:'云网边端一体化',
    activeImgSrc:require('../assets/images/sol3.png')
  }
}
import SolutionItem from '../components/solutionItem'
export default {
  name:'index',
  components:{
    SolutionItem,
  },
  data(){
    return {
      option1:[{
        icon: require('../assets/images/icon1.png'),
        text1:'不破坏章体',
        text2:'合理物理结构，不破坏章体',
        text3:'支持市面98%章型',
      },{
        icon:require('../assets/images/icon2.png'),
        text1:'拍照存档',
        text2:'智能印章机完成盖章同时会',
        text3:'对文件500万PPI拍照',
      },{
        icon:require('../assets/images/icon3.png'),
        text1:'指纹认证',
        text2:'支持账号指纹双重认证',
        text3:'实现限本人使用功能',
      },{
        icon:require('../assets/images/icon4.png'),
        text1:'印章定位',
        text2:'可实现用印次数、时间',
        text3:'坐标、对象多重限制',
      },{
        icon:require('../assets/images/icon5.png'),
        text1:'非法预警',
        text2:'内置多种传感器、报警机制',
        text3:'避免各种非法操作',
      }],
      activeName:'first',
      // activeTabObj:{
      //   activeName:'本地私有一体化',
      //   activeImgSrc:'../assets/images/sol1.png'
      // }
    }
  },
  computed:{},
  watch:{},
  methods:{
    // handleClick({name}, event) {
    //   console.log(tab, event);
    //   if(name != this.activeName){
    //     this.activeTabObj = o[name]
    //   }
    // }
  },
}
</script>

<style lang="scss"> 
.index-page {
  min-height: 100vh;
  width: 100vw;
  .header-div{
    width: 100%;
    height: 500px;
    background: url('../assets/images/header-bg.png');
    background-repeat: no-repeat;
    background-size:100% 100%;
  }
  .header-nav-div{
    width: 100%;
    height: 50px;
    line-height: 50px;
    background: rgba(255, 255, 255, 0.1);
    .login-warpper{
      display: flex;
      justify-content: flex-end;
      width: 1146px;
      margin: 0 auto;
      .handle-view{
        width: 1146px;
        width: 465px;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: space-around;
        .item{
          font-size: 14px;
          font-family: Microsoft YaHei;
          font-weight: 400;
          color: #000000;
        }
        .register{
          width: 80px;
          height: 36px;
          line-height: 36px;
          background: #E12128;
          text-align: center;
          border-radius: 4px;
          font-size: 14px;
          font-family: Microsoft YaHei;
          font-weight: 400;
          color: #FFFFFF;
        }
      }
    }
  }
  .nav-div{
    width: 100%;
    height: 68px;
    background: rgba(255, 255, 255, 0.2);
    .nav-div-warp{
      width: 100%;
      width: 1146px;
      height: 100%;
      margin: 0 auto;
      .nav-div-warp-box{
        display: flex;
        width: 899px;
        height: 68px;
        align-items: center;
        line-height: 68px;
        justify-content: space-between;
        .logo-div{
          width: 115px;
          height: 36px;
          margin: 0 auto;
          img{
            width: 100%;
            height: 100%;
          }
        }
        .text-div{
          display: flex;
          width: 681px;
          justify-content: space-around;
          .item{
            font-size: 16px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #000;
          }
        }
      }
    }
  }
  .banner-div{
    width: 100%;
    height: 384px;
    .banner-div-warp{
      width: 1164px;
      margin: 0 auto;
      .banner-div-warp__box{
        display: flex;
        width: 925px;
        justify-content: space-between;
        .box-left{
          margin-top: 122px;
          margin-left: 170px;
          .text{
            font-size: 30px;
            font-family: Microsoft YaHei;
            font-weight: bold;
            color: #000000;
            span{
              color: #E20B13;
              font-size: 34.29px;
            }
          }
          .btn{
            width: 120px;
            height: 44px;
            text-align: center;
            line-height: 44px;
            background: #E12128;
            border-radius: 4px;
            font-size: 18px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #FFFFFF;
            margin-top: 31px;
          }
        }
        .box-right{
          width: 221px;
          height: 374px;
          margin-top: 43px;
        }
      }
    }
  }
  .banner-bottom-div{
    width: 100%;
    height: 175px;
    background: #F8F8FA;
    .banner-bottom-div-warp{
      width: 1362px;
      height: 100%;
      margin: 0 auto;
      display: flex;
      justify-content: center;
      .banner-bottom-div-warp__box{
        display: flex;
        width: 1362px;
        justify-content: space-around;
        align-items: center;
        .item{
          text-align: center;
          .icon-div{
            width: 40px;
            height: 46px;
            margin: 0 auto;
          }
          .text-1{
            font-size: 18px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #000000;
            margin: 11px 0 13px;
          }
          .text-2{
            font-size: 12px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #000000;
            line-height: 20px;
            opacity: 0.6;
          }
          .text-3{
            font-size: 12px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #000000;
            line-height: 20px;
            opacity: 0.6;
          }
        }
      }
    }
  }
  .solution-div{
    width: 100%;
    height: 702px;
    background: #FFFFFF;
    .solution-div-warp{
      // width: 1146px;
      // height: 100%;
      // margin: 0 auto;
      .title-div{
        width: 100%;
        text-align: center;
        padding-top: 58px;
        .text-1{
          font-size: 28px;
          font-family: Microsoft YaHei;
          font-weight: 400;
          color: #22272A;
          margin-bottom: 19px;
        }
        .text-2{
          font-size: 18px;
          font-family: Microsoft YaHei;
          font-weight: 400;
          color: #000000;
          opacity: 0.6;
          margin-bottom: 50px;
        }
      }
      .tabs-div-warp{
        width: 100vw;
        height: 43px;
        border-bottom: 1px solid #F1F2F5;
        .tabs-div{
          display: flex;
          justify-content: center;
          .el-tabs__item{
            font-size: 18px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #000000;
            height: 43px;
            line-height: 43px;
            opacity: 0.7;
            padding:0 80px;
          }
          .el-tabs__item.is-active{
            color: #FF1616;
          }
          .el-tabs__item:hover{
            color: #FF1616;
          }
          .el-tabs__nav-wrap::after{
            background-color:#F1F2F5;
            height: 1px;
          }
        }
        .first {
          .el-tabs__active-bar{
            background: #FF1616;
            width: 169px !important;
            transform: translateX(61px) !important;
          }
        }
        .second {
          .el-tabs__active-bar{
            background: #FF1616;
            width: 169px !important;
            transform: translateX(347px) !important;
          }
        }
        .third {
          .el-tabs__active-bar{
            background: #FF1616;
            width: 169px !important;
            transform: translateX(633px) !important;
          }
        }
      }
    }
  }
}

</style>

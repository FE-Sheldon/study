<template>
  <div class="solutionItem-component">
    <div class="container">
      <div class="left-box" :class="'left-box-' + activeName">
        <img :src="activeObj.activeImgSrc" alt="" srcset="">
      </div>
      <div class="right-box">
        <div class="text-1">{{activeObj.activeText}}</div>
        <div class="text-2" :class="activeName">{{activeObj.activeText2}}</div>
        <div class="config-message-box" v-show="activeName === 'first'">
          <div class="left">
            <div class="title">服务器配置:</div>
            <div class="text-3 text"><img src="../assets/images/success-icon.png" width="16" height="13" alt="" srcset="">CPU型号： Intel XeonE3</div>
            <div class="text-4 text"><img src="../assets/images/success-icon.png" width="16" height="13" alt="" srcset="">内存：  16G以上</div>
            <div class="text-5 text"><img src="../assets/images/success-icon.png" width="16" height="13" alt="" srcset="">硬盘：  1T</div>
          </div>
          <div class="right">
            <div class="title">操作系统:</div>
            <div class="text-6 text">CentOS 6.5以上</div>
          </div>
        </div>

        <div class="config-message-box" v-show="activeName === 'second'">
          <div class="icon-box">
            <img src="../assets/images/aly-icon.png" width="73" height="27" alt="" srcset="">
            <img src="../assets/images/hwy-icon.png" width="87" height="32" alt="" srcset="">
            <img src="../assets/images/txy-icon.png" width="70" height="26" alt="" srcset="">
          </div>
        </div>

        <div class="config-message-box" v-show="activeName === 'third'">
          <div class="left">
            <div class="text-3 text"><img src="../assets/images/success-icon.png" width="16" height="13" alt="" srcset="">物理服务器</div>
            <div class="text-4 text"><img src="../assets/images/success-icon.png" width="16" height="13" alt="" srcset="">企业云平台</div>
            <div class="text-5 text"><img src="../assets/images/success-icon.png" width="16" height="13" alt="" srcset="">对象存储</div>
          </div>
          <div class="right">
            <div class="text-3 text"><img src="../assets/images/success-icon.png" width="16" height="13" alt="" srcset="">专属私有网络VP</div>
            <div class="text-4 text"><img src="../assets/images/success-icon.png" width="16" height="13" alt="" srcset="">虚拟主机</div>
            <div class="text-5 text"><img src="../assets/images/success-icon.png" width="16" height="13" alt="" srcset="">统一认证</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
const options = {
  first:{
    activeText:'本地私有一体化',
    activeText2:'适合中小型企业使用，秒级交付速度 100%数据  网络隔离 安全可靠',
    activeImgSrc:require('@/assets/images/sol1.png')
  },
  second:{
    activeText:'公私混托一体化',
    activeText2:'适合大型企业使用，在公有云上私有化部署 分部于公私外网统一使用，数据安全保密',
    activeImgSrc:require('@/assets/images/sol2.png')
  },
  third:{
    activeText:'云网边端一体化',
    activeText2:'适合上市公司云网融合架构，通过云和网的深入融合与高度协同，延展云边端构成的全域 数字化场景，构建 “云+网+应用” 一站式业务',
    activeImgSrc:require('@/assets/images/sol3.png')
  }
}
export default {
  props:['activeName'],
  data(){
    return {
      activeObj:{}
    }
  },
  mounted(){
    this.activeObj = options[this.activeName]
    console.warn(this.activeName)
  },
}
</script>

<style lang="scss" scoped>
.solutionItem-component{
  .container{
    display: flex;
    margin-top: 56px;
    .left-box{
      // width: 322px;
      // height: 309px;
      margin-right: 160.9px;
    }
    .left-box-third{
      margin-right:50px;
    }
    .right-box{
      .text-1{
        font-size: 20px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #000000;
        margin: 17px 0 23px;
      }
      .text-2{
        font-size: 16px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: #000000;
        margin-bottom: 54px;
      }
      .first{
        width: 256px;
      }
      .second{
        width: 304px;
      }
      .third{
        width: 395px;
        font-size: 14px;
      }
      .config-message-box{
        display: flex;
        .title{
          font-size: 14px;
          font-family: Microsoft YaHei;
          font-weight: 400;
          color: #666666;
          margin-bottom: 21px;
        }
        .text{
          font-size: 14px;
          font-family: Microsoft YaHei;
          font-weight: 400;
          color: #000000;
          img{
            margin-right: 9.8px;
          }
        }
        .right{
          margin-left: 47px;
        }
        .text-4{
          margin: 15px 0;
        }
      }
    }
  }
}
</style>>

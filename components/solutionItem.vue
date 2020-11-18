<template>
  <div class="solutionItem-component">
    <div class="container">
      <div class="left-box">
        <img :src="activeObj.activeImgSrc" alt="" srcset="">
      </div>
      <div class="right-box">
        <div class="text-1">{{activeObj.activeText}}</div>
        <div class="text-2">适合中小型企业使用，秒级交付速度 100%数据  网络隔离 安全可靠</div>
        <div class="config-message-box">
          <div class="left">
            <div class="title">服务器配置:</div>
            <div class="text-3 text">CPU型号： Intel XeonE3</div>
            <div class="text-4 text">内存：  16G以上</div>
            <div class="text-5 text">硬盘：  1T</div>
          </div>
          <div class="right">
            <div class="title">操作系统:</div>
            <div class="text-6 text">CentOS 6.5以上</div>
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
    activeImgSrc:require('@/assets/images/sol1.png')
  },
  second:{
    activeText:'公私混托一体化',
    activeImgSrc:require('@/assets/images/sol2.png')
  },
  third:{
    activeText:'云网边端一体化',
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
    console.warn(this.activeObj)
  },
}
</script>

<style lang="scss" scoped>
.solutionItem-component{
  .container{
    display: flex;
    margin-top: 56px;
    .left-box{
      width: 322px;
      height: 309px;
      margin-right: 160.9px;
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
        width: 256px;
        font-size: 16px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: #000000;
        margin-bottom: 54px;
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

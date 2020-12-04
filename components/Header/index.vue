<template>
  <div class="header-components">
    <!-- 登陆注册 -->
    <div class="header-nav-div">
      <div class="login-warpper">
        <div class="handle-view">
          <div class="item">API接口</div>
          <div class="item">下载应用</div>
          <div class="item">帮助</div>
          <div class="item" style="color: #e12128">云平台登陆</div>
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
            <img src="@/assets/images/logo.png" alt="" srcset="" />
          </div>
          <div class="text-div">
            <div class="item" v-for="item in navOption" :key="item.name" @click="handleClickNav(item.routeName)" :class="$route.name === item.routeName ? 'active':''">{{item.name}}</div>
          </div>
        </div>
      </div>
    </div>
    <!-- 导航end -->
  </div>
</template>

<script>
export default {
  name:'Header',
  data(){
    return {
      navOption:[{
        name:'首页',
        routeName:'index',
      },{
        name:'解决方案',
        routeName:'solution',
      },{
        name:'产品',
        routeName:'product',
      },{
        name:'客户案例',
        routeName:'customerCase',
      },{
        name:'服务与支持',
        routeName:'serviceSupport',
      },{
        name:'联系我们',
        routeName:'contactWe',
      }]
    }
  },
  mounted(){
    console.warn(this.$route)
  },
  methods: {
    handleClickNav(name) {
      this.$router.push({name})
      // document.querySelector(id).scrollIntoView(true);
    },
  },
};
</script>

<style lang="scss" scoped>
.header-components {
  .header-nav-div {
    width: 100%;
    height: 50px;
    line-height: 50px;
    background: rgba(255, 255, 255, 0.1);
    .login-warpper {
      display: flex;
      justify-content: flex-end;
      width: 1146px;
      margin: 0 auto;
      .handle-view {
        width: 1146px;
        width: 465px;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: space-around;
        .item {
          font-size: 14px;
          font-family: Microsoft YaHei;
          font-weight: 400;
          color: #000000;
        }
        .register {
          width: 80px;
          height: 36px;
          line-height: 36px;
          background: #e12128;
          text-align: center;
          border-radius: 4px;
          font-size: 14px;
          font-family: Microsoft YaHei;
          font-weight: 400;
          color: #ffffff;
        }
      }
    }
  }
  .nav-div {
    width: 100%;
    height: 68px;
    background: rgba(255, 255, 255, 0.2);
    .nav-div-warp {
      width: 100%;
      width: 1146px;
      height: 100%;
      margin: 0 auto;
      .nav-div-warp-box {
        display: flex;
        width: 899px;
        height: 68px;
        align-items: center;
        line-height: 68px;
        justify-content: space-between;
        .logo-div {
          width: 115px;
          height: 36px;
          margin: 0 auto;
          img {
            width: 100%;
            height: 100%;
          }
        }
        .text-div {
          display: flex;
          width: 681px;
          justify-content: space-around;
          .item {
            cursor: pointer;
            text-decoration: none;
            display: block;
            font-size: 16px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #000;
          }
          .active {
            color: #DE1C24;
          }
        }
      }
    }
  }
}
</style>
<template>
  <div class="index-page">
    <div class="header-div">
      <!-- banner -->
      <div class="banner-div">
        <div class="banner-div-warp">
          <div class="banner-div-warp__box">
            <div class="box-left">
              <div class="text">不破坏章体 支持章型 <span>98%</span></div>
              <div class="btn">了解详情</div>
            </div>
            <div class="box-right">
              <img src="../assets/images/印章.png" alt="" srcset="" />
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
              <img :src="item.icon" alt="" srcset="" />
            </div>
            <div class="text-1">{{ item.text1 }}</div>
            <div class="text-2">{{ item.text2 }}</div>
            <div class="text-3">{{ item.text3 }}</div>
          </div>
        </div>
      </div>
    </div>
    <!-- 不破坏到非法预警end -->

    <!-- 解决方案 -->
    <div class="solution-div" id="solution">
      <div class="solution-div-warp">
        <div class="title-div">
          <div class="text-1">云网边端一体化解决方案 助力企业数字化转型</div>
          <div class="text-2">思格特智能印章机系统</div>
        </div>
        <div class="tabs-div-warp">
          <div :class="'tabs-div ' + activeName">
            <div>
              <el-tabs v-model="activeName">
                <el-tab-pane label="本地私有一体化" name="first"
                  ><SolutionItem activeName="first"
                /></el-tab-pane>
                <el-tab-pane label="公私混托一体化" name="second"
                  ><SolutionItem activeName="second"
                /></el-tab-pane>
                <el-tab-pane label="云网边端一体化" name="third"
                  ><SolutionItem activeName="third"
                /></el-tab-pane>
              </el-tabs>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- 解决方案end -->

    <!-- 产品 -->
    <div class="product-div" id="product">
      <div class="product-div-warp">
        <div class="product-div-warp__box">
          <div class="product-div-warp__box__left">
            <div
              class="item"
              :class="menuIndex === 1 ? 'active' : ''"
              @click="handleMenuClick({ index: 1, text: '金融行业' })"
            >
              金融行业
            </div>
            <div
              class="item"
              :class="menuIndex === 2 ? 'active' : ''"
              @click="handleMenuClick({ index: 2, text: '地产行业' })"
            >
              地产行业
            </div>
            <div
              class="item"
              :class="menuIndex === 3 ? 'active' : ''"
              @click="handleMenuClick({ index: 3, text: '事业单位' })"
            >
              事业单位
            </div>
            <div
              class="item"
              :class="menuIndex === 4 ? 'active' : ''"
              @click="handleMenuClick({ index: 4, text: '科技单位' })"
            >
              科技单位
            </div>
            <div
              class="item"
              :class="menuIndex === 5 ? 'active' : ''"
              @click="handleMenuClick({ index: 5, text: '交通行业' })"
            >
              交通行业
            </div>
            <div
              class="item"
              :class="menuIndex === 6 ? 'active' : ''"
              @click="handleMenuClick({ index: 6, text: '国企单位' })"
            >
              国企单位
            </div>
          </div>
          <div class="product-div-warp__box__right">
            <div class="top">
              <div class="title-1">智能印章产品行业解决方案</div>
              <div class="title-2">
                思格特SIGNET针对行业特征及细分业务场景深度定制，打造一站式解决方案
              </div>
            </div>
            <div class="center">
              <div class="center-text-1">{{ activeText }}</div>
              <div class="center-text-2">
                为银行、保险、证券、互联网金融等客户提供安全合规、稳定的智能印章设备及可靠的整体解决方案。
              </div>
              <div class="center-btn">
                <div class="center-btn__item">安全合规</div>
                <div class="center-btn__item">物理隔离</div>
                <div class="center-btn__item">稳定可靠</div>
              </div>
            </div>
            <div class="bottom">
              <div class="bottom-text">客户案例</div>
              <div class="bottom-icon">
                <img src="../assets/images/product_icon.png" alt="" srcset="" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- 产品 end -->

    <!-- 客户案例 -->
    <div class="customer-case-div" id="customerCase">
      <div class="customer-case-div-warp">
        <div class="customer-case-div-warp__title">
          <div class="title-text-1">助力企业智能用印管理案例</div>
          <div class="title-text-2">
            思格特SIGNET为您提供安全、稳定、耐用的产品服务，助力企业快速发展
          </div>
          <div class="icon-box">
            <div
              class="icon-box-item"
              v-for="(item, index) in customerIconOption"
              :key="item.src"
            >
              <img
                :src="item.src"
                alt=""
                srcset=""
                :width="item._width"
                :height="item._height"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- 客户案例 end -->

    <!-- 服务与支持 -->
    <div class="service-support-div" id="serviceSupport">
      <div class="service-support-div-warp">
        <div class="service-support-div-warp__title">
          <div class="title-text-1">全国专业服务团队</div>
          <div class="title-text-2">
            思格特SIGNET为您提供专业即时的售后技术服务
          </div>
        </div>
        <div class="service-support-div-warp__content">
          <div
            class="service-support-div-warp__content__item"
            v-for="item in serviceSupportData"
            :key="item.cityName"
          >
            <div class="city-name">{{ item.cityName }}</div>
            <div class="info">
              <div>{{ item.info1 }}</div>
              <div>{{ item.info2 }}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- 服务与支持 end -->

    <div class="service-support-div-bottom">
      <div class="service-support-div-bottom-warp">
        <div class="service-support-div-bottom-warp__box">
          <div
            class="service-support-div-bottom-warp__box__item"
            v-for="item in options2"
            :key="item.src"
          >
            <div class="img-div">
              <img :src="item.src" alt="" />
            </div>
            <div class="text">{{ item.text }}</div>
          </div>
        </div>
      </div>
    </div>

    <!-- 联系我们 -->
    <div class="contact-we-div" id="contactWe">
      <div class="contact-we-div-top">
        <div class="contact-we-div-top__text-1">提交申请，免费安装试用30天</div>
        <div class="contact-we-div-top__btn">现在提交</div>
      </div>
    </div>
    <!-- 联系我们 end -->
  </div>
</template>
<script>
let o = {
  first: {
    activeName: "本地私有一体化",
    activeImgSrc: require("../assets/images/sol1.png"),
  },
  second: {
    activeName: "公私混托一体化",
    activeImgSrc: require("../assets/images/sol2.png"),
  },
  third: {
    activeName: "云网边端一体化",
    activeImgSrc: require("../assets/images/sol3.png"),
  },
};
import SolutionItem from "@/components/solutionItem";
export default {
  name: "index",
  components: {
    SolutionItem,
  },
  data() {
    return {
      options2: [
        {
          src: require("../assets/images/service-support-49.png"),
          text: "公安部信息系统安全等级保护",
        },
        {
          src: require("../assets/images/service-support-50.png"),
          text: "公安部产品安全认证",
        },
        {
          src: require("../assets/images/service-support-51.png"),
          text: "ISO9001质量体系认证",
        },
        {
          src: require("../assets/images/service-support-52.png"),
          text: "中国诚信供应商",
        },
        {
          src: require("../assets/images/service-support-53.png"),
          text: "发明专利",
        },
      ],
      serviceSupportData: [
        {
          cityName: "北京",
          info1: "北京市朝阳区望京SoHo",
          info2: "T2.3.1806",
        },
        {
          cityName: "上海",
          info1: "北京市朝阳区望京SoHo",
          info2: "T2.3.1806",
        },
        {
          cityName: "上海",
          info1: "北京市朝阳区望京SoHo",
          info2: "T2.3.1806",
        },
        {
          cityName: "北京",
          info1: "北京市朝阳区望京SoHo",
          info2: "T2.3.1806",
        },
        {
          cityName: "上海",
          info1: "北京市朝阳区望京SoHo",
          info2: "T2.3.1806",
        },
        {
          cityName: "上海",
          info1: "北京市朝阳区望京SoHo",
          info2: "T2.3.1806",
        },
      ],
      customerIconOption: [
        {
          src: require(`../assets/images/coustomer-case-25.png`),
          _width: "114px",
          _height: "74px",
        },
        {
          src: require(`../assets/images/coustomer-case-26.png`),
          _width: "103px",
          _height: "86px",
        },
        {
          src: require(`../assets/images/coustomer-case-27.png`),
          _width: "133px",
          _height: "61px",
        },
        {
          src: require(`../assets/images/coustomer-case-28.png`),
          _width: "123px",
          _height: "75px",
        },
        {
          src: require(`../assets/images/coustomer-case-29.png`),
          _width: "97px",
          _height: "73px",
        },
        {
          src: require(`../assets/images/coustomer-case-30.png`),
          _width: "124px",
          _height: "74px",
        },
        {
          src: require(`../assets/images/coustomer-case-31.png`),
          _width: "134px",
          _height: "53px",
        },
        {
          src: require(`../assets/images/coustomer-case-32.png`),
          _width: "131px",
          _height: "66px",
        },
        {
          src: require(`../assets/images/coustomer-case-33.png`),
          _width: "115px",
          _height: "32px",
        },
        {
          src: require(`../assets/images/coustomer-case-34.png`),
          _width: "87px",
          _height: "81px",
        },
        {
          src: require(`../assets/images/coustomer-case-35.png`),
          _width: "131px",
          _height: "70px",
        },
        {
          src: require(`../assets/images/coustomer-case-36.png`),
          _width: "135px",
          _height: "50px",
        },
        {
          src: require(`../assets/images/coustomer-case-37.png`),
          _width: "134px",
          _height: "61px",
        },
        {
          src: require(`../assets/images/coustomer-case-38.png`),
          _width: "95px",
          _height: "74px",
        },
        {
          src: require(`../assets/images/coustomer-case-39.png`),
          _width: "122px",
          _height: "60px",
        },
        {
          src: require(`../assets/images/coustomer-case-40.png`),
          _width: "135px",
          _height: "52px",
        },
        {
          src: require(`../assets/images/coustomer-case-41.png`),
          _width: "122px",
          _height: "54px",
        },
        {
          src: require(`../assets/images/coustomer-case-42.png`),
          _width: "115px",
          _height: "67px",
        },
        {
          src: require(`../assets/images/coustomer-case-43.png`),
          _width: "109px",
          _height: "65px",
        },
        {
          src: require(`../assets/images/coustomer-case-44.png`),
          _width: "128px",
          _height: "63px",
        },
      ],
      option1: [
        {
          icon: require("../assets/images/icon1.png"),
          text1: "不破坏章体",
          text2: "合理物理结构，不破坏章体",
          text3: "支持市面98%章型",
        },
        {
          icon: require("../assets/images/icon2.png"),
          text1: "拍照存档",
          text2: "智能印章机完成盖章同时会",
          text3: "对文件500万PPI拍照",
        },
        {
          icon: require("../assets/images/icon3.png"),
          text1: "指纹认证",
          text2: "支持账号指纹双重认证",
          text3: "实现限本人使用功能",
        },
        {
          icon: require("../assets/images/icon4.png"),
          text1: "印章定位",
          text2: "可实现用印次数、时间",
          text3: "坐标、对象多重限制",
        },
        {
          icon: require("../assets/images/icon5.png"),
          text1: "非法预警",
          text2: "内置多种传感器、报警机制",
          text3: "避免各种非法操作",
        },
      ],
      menuIndex: 1,
      activeName: "first",
      activeText: "金融行业",
      // activeTabObj:{
      //   activeName:'本地私有一体化',
      //   activeImgSrc:'../assets/images/sol1.png'
      // }
    };
  },
  mounted() {},
  computed: {},
  watch: {},
  methods: {
    handleMenuClick({ index, text }) {
      if (index !== this.menuIndex) {
        this.menuIndex = index;
        this.activeText = text;
      }
    },
  },
};
</script>

<style lang="scss">
.index-page {
  min-height: 100vh;
  width: 100vw;
  .header-div {
    width: 100%;
    height: 500px;
    background: url("../assets/images/header-bg.png");
    background-repeat: no-repeat;
    background-size: 100% 100%;
  }
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
        }
      }
    }
  }
  .banner-div {
    width: 100%;
    height: 384px;
    .banner-div-warp {
      width: 1164px;
      margin: 0 auto;
      .banner-div-warp__box {
        display: flex;
        width: 925px;
        justify-content: space-between;
        .box-left {
          margin-top: 122px;
          margin-left: 170px;
          .text {
            font-size: 30px;
            font-family: Microsoft YaHei;
            font-weight: bold;
            color: #000000;
            span {
              color: #e20b13;
              font-size: 34.29px;
            }
          }
          .btn {
            width: 120px;
            height: 44px;
            text-align: center;
            line-height: 44px;
            background: #e12128;
            border-radius: 4px;
            font-size: 18px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #ffffff;
            margin-top: 31px;
          }
        }
        .box-right {
          width: 221px;
          height: 374px;
          margin-top: 43px;
        }
      }
    }
  }
  .banner-bottom-div {
    width: 100%;
    height: 175px;
    background: #f8f8fa;
    .banner-bottom-div-warp {
      width: 1362px;
      height: 100%;
      margin: 0 auto;
      display: flex;
      justify-content: center;
      .banner-bottom-div-warp__box {
        display: flex;
        width: 1362px;
        justify-content: space-around;
        align-items: center;
        .item {
          text-align: center;
          .icon-div {
            width: 40px;
            height: 46px;
            margin: 0 auto;
          }
          .text-1 {
            font-size: 18px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #000000;
            margin: 11px 0 13px;
          }
          .text-2 {
            font-size: 12px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #000000;
            line-height: 20px;
            opacity: 0.6;
          }
          .text-3 {
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
  .solution-div {
    width: 100%;
    height: 702px;
    background: #ffffff;
    .solution-div-warp {
      // width: 1146px;
      // height: 100%;
      // margin: 0 auto;
      .title-div {
        width: 100%;
        text-align: center;
        padding-top: 58px;
        .text-1 {
          font-size: 28px;
          font-family: Microsoft YaHei;
          font-weight: 400;
          color: #22272a;
          margin-bottom: 19px;
        }
        .text-2 {
          font-size: 18px;
          font-family: Microsoft YaHei;
          font-weight: 400;
          color: #000000;
          opacity: 0.6;
          margin-bottom: 50px;
        }
      }
      .tabs-div-warp {
        width: 100vw;
        height: 43px;
        border-bottom: 1px solid #f1f2f5;
        .tabs-div {
          display: flex;
          justify-content: center;
          .el-tabs__item {
            font-size: 18px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #000000;
            height: 43px;
            line-height: 43px;
            opacity: 0.7;
            padding: 0 80px;
          }
          .el-tabs__item.is-active {
            color: #ff1616;
          }
          .el-tabs__item:hover {
            color: #ff1616;
          }
          .el-tabs__nav-wrap::after {
            background-color: #f1f2f5;
            height: 1px;
          }
        }
        .first {
          .el-tabs__active-bar {
            background: #ff1616;
            width: 169px !important;
            transform: translateX(61px) !important;
          }
        }
        .second {
          .el-tabs__active-bar {
            background: #ff1616;
            width: 169px !important;
            transform: translateX(347px) !important;
          }
        }
        .third {
          .el-tabs__active-bar {
            background: #ff1616;
            width: 169px !important;
            transform: translateX(633px) !important;
          }
        }
      }
    }
  }
  .product-div {
    width: 100%;
    height: 581px;
    background: url("../assets/images/product_bg.png");
    background-repeat: no-repeat;
    background-size: 100% 100%;
    .product-div-warp {
      width: 1146px;
      margin: 0 auto;
      .product-div-warp__box {
        display: flex;
        .product-div-warp__box__left {
          width: 250px;
          height: 579px;
          background: rgba($color: #232323, $alpha: 0.8);
          padding: 121px 0;
          box-sizing: border-box;
          .item {
            font-size: 16px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: rgba($color: #ffffff, $alpha: 0.6);
            text-align: center;
            width: 250px;
            height: 50px;
            line-height: 50px;
          }
          .item:hover {
            cursor: pointer;
          }
          .active {
            background: #c6272e;
            color: #ffffff;
          }
        }
        .product-div-warp__box__right {
          margin-left: 79px;
          .top {
            text-align: center;
            .title-1 {
              font-size: 30px;
              font-family: Microsoft YaHei;
              font-weight: 400;
              color: #ffffff;
              margin: 60px 0 23px;
            }
            .title-2 {
              font-size: 16px;
              font-family: Microsoft YaHei;
              font-weight: 400;
              color: rgba($color: #ffffff, $alpha: 0.6);
            }
          }
          .center {
            margin: 73px 0 70.7px;
            .center-text-1 {
              font-size: 23px;
              font-family: Microsoft YaHei;
              font-weight: bold;
              color: #ffffff;
            }
            .center-text-2 {
              font-size: 15px;
              font-family: Microsoft YaHei;
              font-weight: 400;
              color: #ffffff;
              margin: 39px 0 24.3px;
            }
            .center-btn {
              display: flex;
              .center-btn__item {
                margin-right: 11px;
                width: 76px;
                height: 24px;
                background: #c4181f;
                border-radius: 4px;
                text-align: center;
                line-height: 24px;
                font-size: 13px;
                font-family: Microsoft YaHei;
                font-weight: 300;
                color: #ffffff;
              }
            }
          }
          .bottom {
            .bottom-text {
              font-size: 13px;
              font-family: Microsoft YaHei;
              font-weight: 300;
              color: #ffffff;
            }
            .bottom-icon {
              widows: 116px;
              height: 30px;
              margin-top: 19px;
            }
          }
        }
      }
    }
  }
  .customer-case-div {
    width: 100%;
    height: 710px;
    background: #fff;
    .customer-case-div-warp {
      width: 1146px;
      margin: 0 auto;
      .title-text-1 {
        text-align: center;
        font-size: 30px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: #000000;
        margin: 51px 0 23px;
      }
      .title-text-2 {
        text-align: center;
        font-size: 16px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: rgba($color: #000000, $alpha: 0.9);
      }
    }
    .icon-box {
      display: flex;
      flex-wrap: wrap;
      width: 1026px;
      height: 423px;
      justify-content: space-around;
      margin: 79.5px auto 0;
      .icon-box-item {
        width: 198px;
        height: 99px;
        background: #ffffff;
        border: 1px solid #f2f2f2;
        display: flex;
        justify-content: center;
        align-items: center;
      }
    }
  }
  .service-support-div {
    width: 100%;
    height: 468px;
    background: url("../assets/images/service-support-bg.png");
    background-repeat: no-repeat;
    background-size: 100% 100%;
    .service-support-div-warp {
      width: 1146px;
      height: 100%;
      margin: auto;
      .service-support-div-warp__title {
        overflow: hidden;
        text-align: center;
        .title-text-1 {
          font-size: 30px;
          font-family: Microsoft YaHei;
          font-weight: 400;
          color: #000000;
          margin: 67px 0 21px;
        }
        .title-text-2 {
          font-size: 16px;
          font-family: Microsoft YaHei;
          font-weight: 400;
          color: rgba($color: #000000, $alpha: 0.6);
        }
      }
      .service-support-div-warp__content {
        display: flex;
        width: 920px;
        height: 140px;
        justify-content: space-around;
        margin: 88px auto 0;
        flex-wrap: wrap;
        .service-support-div-warp__content__item {
          display: flex;
          width: 250px;
          .city-name {
            width: 56px;
            height: 25px;
            background: #dc0009;
            text-align: center;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 16px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #ffffff;
            margin-right: 9px;
          }
          .info {
            font-size: 15px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #000000;
          }
        }
      }
    }
  }
  .service-support-div-bottom {
    width: 100%;
    height: 140px;
    background: #ffffff;
    .service-support-div-bottom-warp {
      width: 1188px;
      margin: 0 auto;
      height: 100%;
      .service-support-div-bottom-warp__box {
        display: flex;
        width: 1157px;
        height: 100%;
        justify-content: space-around;
        align-items: center;
        .service-support-div-bottom-warp__box__item {
          text-align: center;
          .text {
            font-size: 13px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #0d0d0d;
            margin-top: 14px;
          }
        }
      }
    }
  }
  .contact-we-div {
    width: 100%;
    height: 529px;
    .contact-we-div-top {
      text-align: center;
      width: 100%;
      height: 179px;
      overflow: hidden;
      background: rgba($color: #000000, $alpha: 0.9);
      background: url("../assets/images/contact-we-bg.png");
      background-repeat: no-repeat;
      background-size: 100% 100%;
      .contact-we-div-top__text-1 {
        font-size: 18px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: #fefefe;
        margin: 42px 0 29px;
      }
      .contact-we-div-top__btn {
        width: 160px;
        height: 44px;
        margin: 0 auto;
        line-height: 44px;
        text-align: center;
        background: #c6272e;
        border-radius: 4px;
        font-size: 18px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: #fefefe;
      }
    }
  }
}
</style>

<template>
  <div class="footer-components">
    <div class="contact-we-div-center">
      <div class="contact-we-div-center-warp">
        <div class="contact-we-div-center-warp__box">
          <!-- <div class="contact-we-div-center-warp__box__left">
                <div>
                  <img src="@/assets/images/contact-we-54.png" alt="" srcset="">
                </div>
                <div class="center-icon">
                  <img src="@/assets/images/contact-we-55.png" alt="" srcset="">
                </div>
                <div>
                  <img src="@/assets/images/contact-we-56.png" alt="" srcset="">
                </div>
              </div> -->
          <!-- <div class="contact-we-div-center-warp__box__right"> -->
          <div class="item item-icon">
            <div>
              <img src="@/assets/images/contact-we-54.png" alt="" srcset="" />
            </div>
            <div class="center-icon">
              <img src="@/assets/images/contact-we-55.png" alt="" srcset="" />
            </div>
            <div>
              <img src="@/assets/images/contact-we-56.png" alt="" srcset="" />
            </div>
          </div>
          <div class="item">
            <div class="contact-we-text-1">关于我们</div>
            <div class="contact-we-text-2">企业动态</div>
            <div class="contact-we-text-2">案例新闻</div>
          </div>
          <div class="item">
            <div class="contact-we-text-1">产品</div>
            <div class="contact-we-text-2">便携智能印章机</div>
            <div class="contact-we-text-2">AI智能印控台</div>
          </div>
          <div class="item">
            <div class="contact-we-text-1">服务与支持</div>
            <div class="contact-we-text-2">私有化</div>
            <div class="contact-we-text-2">API接口</div>
          </div>
          <div class="item">
            <div class="contact-we-text-1">联系我们</div>
            <div class="contact-we-text-2">400-1123-214</div>
            <div class="contact-we-text-2">185-1472-3986</div>
            <div class="contact-we-text-2">18514723986@139.com</div>
            <div class="contact-we-text-2">北京市朝阳区望京SoHo.T2.3.1806</div>
          </div>
          <!-- </div> -->
        </div>
      </div>
    </div>

    <div class="contact-we-div-bottom">京ICP备20030702号-1</div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.footer-components {
  .contact-we-div-center {
    width: 100%;
    height: 300px;
    background: #181818;
    .contact-we-div-center-warp {
      width: 1146px;
      height: 100%;
      margin: 0 auto;
      overflow: hidden;
      .contact-we-div-center-warp__box {
        display: flex;
        width: 1125px;
        margin: 54px auto 0;
        justify-content: space-around;

        .item {
          .contact-we-text-1 {
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: rgba($color: #ffffff, $alpha: 0.6);
            margin-bottom: 34px;
          }
          .contact-we-text-2 {
            font-size: 13px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: rgba($color: #ffffff, $alpha: 0.8);
            margin-bottom: 18px;
          }
        }
        .item-icon {
          text-align: center;
        }
        .center-icon {
          margin: 2px 0 21px;
        }
        // .contact-we-div-center-warp__box__left{
        //   width: 103px;
        //   text-align: center;
        //   .center-icon{
        //     margin: 2px 0 21px;
        //   }
        // }
        // .contact-we-div-center-warp__box__right{
        //   margin-left: 117px;
        //   display: flex;
        //   width: 802px;
        // }
      }
    }
  }
  .contact-we-div-bottom {
    width: 100%;
    height: 50px;
    line-height: 50px;
    text-align: center;
    background: #151515;
    font-size: 13px;
    font-family: Microsoft YaHei;
    font-weight: 400;
    color: rgba($color: #ffffff, $alpha: 0.8);
  }
}
</style>
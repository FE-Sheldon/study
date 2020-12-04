<template>
  <div class="solution-page">
    <div class="view">
      <div class="view-warp">
        <div class="view-warp-box">
          <div class="left-box">
            <p class="text-1">云+端+智能 一站式印章管理解决方案</p>
            <p class="text-2">
              利用思格特便携机与AI印控台相结合的方法，减轻印章管理员的工作量，并且后台可以留存数据
              以后可追溯。通过OA对接，解决方便用印问题
            </p>
            <div class="btn">立即咨询</div>
          </div>
          <div class="right-box">
            <img src="@/assets/images/solution/79.png" alt="" srcset="" />
          </div>
        </div>
      </div>
    </div>

    <div class="view2">
      <div class="view2-warp">
        <div class="view2-warp-box">
          <div class="left-box">
            <p class="text-1">思格特智能设备简介</p>
            <div class="icon">
              <img src="@/assets/images/solution/内容.png" alt="" />
            </div>
            <p class="text-2">
              思格特智能盖章设备有
              <span>便携式和AI印控台</span> 两种设备满足客户不同需求
            </p>
            <p class="text-2 text-3">
              > 便携式智能盖章设备（以下简称为“便携机”）方便外带使
            </p>
            <p class="text-2 text-4">
              > AI印控台设备（以下简称为“高拍仪”）主要是辅助便携机，
            </p>
            <p class="text-2 text-5">
              加大办公区管理力度，实现自主办公的目的。
            </p>
          </div>
          <div class="right-box">
            <img src="@/assets/images/solution/图.png" alt="" srcset="" />
          </div>
        </div>
      </div>
    </div>

    <div class="view3">
      <div class="view3-warp">
        <p class="title-1">便携式外带用印设备</p>
        <div class="icon">
          <img src="@/assets/images/solution/内容.png" alt="" />
        </div>
        <div class="view3-warp-box">
          <div class="left-box">
            <div>
              <img src="@/assets/images/solution/头图1.png" alt="" />
            </div>
          </div>
          <div class="right-box">
            <div class="head">设备性能参数</div>
            <div class="item">
              <div class="item-left">额定电压： DC5V 1.2A</div>
              <div class="item-right">电池： 2000m/h （持续盖印>500次)</div>
            </div>
            <div class="item">
              <div class="item-left">设备尺寸： 70*200mm-0.58kg</div>
              <div class="item-right">摄像头：500万像素</div>
            </div>
            <div class="item">
              <div class="item-left">用户鉴权： 指纹登录</div>
              <div class="item-right">骑缝章： 支持</div>
            </div>
            <div class="item">
              <div class="item-left">工作温度：-10℃+40℃</div>
              <div class="item-right">印章个数： 1枚（支持各类型实体印章）</div>
            </div>
            <div class="item">
              <div class="item-left">网络： WIGI/4G（外设）</div>
              <div class="item-right">解锁盖印时间： 1.2-2秒</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="view4">
      <div class="view4-warp">
        <p class="title-2">铝合金外壳一体成型</p>
        <div class="btn-box">
          <div class="item">一体成型设计优美</div>
          <div class="item">体积小重量轻</div>
          <div class="item">兼容多种型号</div>
        </div>
        <div class="img">
          <img src="@/assets/images/solution/便携机外壳.png" alt="" />
        </div>
      </div>
    </div>

    <div class="view5">
      <div class="view5-warp">
        <p class="title">便携机结构图</p>
        <div class="img">
          <img
            src="@/assets/images/solution/便携机设备结构图.png"
            alt=""
            srcset=""
          />
        </div>
      </div>
    </div>

    <div class="view6">
      <div class="view6-warp">
        <p class="title-2">物理印章装配兼容性</p>
        <div class="icon">
          <img src="@/assets/images/solution/内容.png" alt="" />
        </div>
        <p class="title-3">
          经过上百种印章试验后，目前思格特便携机在不破坏原印章的情况下能够兼容所有类型、所有形状的印章，并且兼容直径45mm范围内所有
        </p>
        <div class="header">思格特印章兼容表</div>
        <table
          class="view6-warp-table"
          border="0"
          cellspacing="0"
          cellpadding="0"
        >
          <tr class="item-tr-1">
            <td class="item-td-1">类型</td>
            <td>圆形</td>
            <td>椭圆形</td>
            <td>方形</td>
            <td>长方形</td>
            <td style="width: 262px;">其他</td>
          </tr>
          <tr v-for="item in tableData" :key="item.type">
            <td class="item-td-1">{{ item.type }}</td>
            <td>兼容</td>
            <td>兼容</td>
            <td>兼容</td>
            <td>兼容</td>
            <td style="width: 262px;">5个工作日定制</td>
          </tr>
        </table>

        <div class="view6-warp-img">
          <img src="@/assets/images/solution/表格2.png" alt="" />
        </div>
      </div>
    </div>

    <div class="view7">
      <div class="view7-warp">
        <p class="title-2">装配操作 · 印章安装</p>
        <p class="title-3">
          思格特智能印章设备给客户配有专门印章套，把原印章装进印章套即可配套设备使用，
        </p>
        <p class="title-3">无需对用户原有印章进行切割或任何改装，不破坏原有</p>
        <div class="icon">
          <img src="@/assets/images/solution/内容.png" alt="" />
        </div>
        <div class="header">思格特印章套件安装例图</div>
        <div class="view7-warp-img">
          <img src="@/assets/images/solution/表格.png" alt="" />
        </div>
      </div>
    </div>

    <div class="view8">
      <div class="view8-warp">
        <p class="title-1">用印设备盖章与实际用印文件一致性</p>
        <div class="icon">
          <img src="@/assets/images/solution/内容.png" alt="" />
        </div>

        <div class="view8-warp-box">
          <div class="view8-warp-box-left view8-warp-box-item">
            <div class="container">
              <div class="xuhao">1</div>
              <div class="title">信息记录</div>
            </div>
            <div class="message">
              思格特智能印章设备每次用印都会生成用印记录，包括用印人、用印时间、印章信息等内容，并且设备内置有500万像素高清摄像头，每一次用印瞬间都会自动触发拍照且立即上传用印照片和用印信息到云服务器，用户可以通过后台记录对盖印图片与真实文件做对比。
            </div>
            <div class="img">
              <img src="@/assets/images/solution/配图2.png" alt="" />
            </div>
          </div>
          <div class="view8-warp-box-right view8-warp-box-item">
            <div class="img">
              <img src="@/assets/images/solution/配图1.png" alt="" />
            </div>
            <div class="container">
              <div class="xuhao">2</div>
              <div class="title">关于设计</div>
            </div>
            <div class="message">
              在摄像头设计上，目前市面上有摄像头一体式便携盖章机和摄像头分离式便携盖章机两种类型。思格特便携机采用500万像素摄像头集成于机身，每次用印自动拍照，盖哪拍哪，杜绝假冒用章行为。
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="view9">
      <div class="view9-warp">
        <p class="title-1">提供两种用印模式</p>
        <div class="img">
          <img src="@/assets/images/solution/内容.png" alt="" />
        </div>
        <div class="view9-warp-model">
          <div class="view9-warp-model-box">
            <div class="model-item model-left">
              <p class="p-1">授权用印模式</p>
              <p class="p-2">使用方法：</p>
              <div class="content content-1">
                <img src="@/assets/images/solution/形状8拷贝.png" alt="" />
                <span>
                  用APP端或者PC端申请授权并启动盖印，盖印信息及盖印照片即时
                  上传到云服务器，可供随时查看。
                </span>
              </div>
              <div class="content content-2">
                <img src="@/assets/images/solution/形状8拷贝.png" alt="" />
                <span>
                  通过申请和审批来控制印章的使用。可限定使用次数，限定使用地点、
                  限定使用时间段等控制使用范围。
                </span>
              </div>
              <div class="content content-3">
                <img src="@/assets/images/solution/形状8拷贝.png" alt="" />
                <span> 开锁时间 0.3秒 </span>
              </div>
            </div>
            <div class="model-item model-right">
              <p class="p-1">本地用印模式</p>
              <p class="p-2">使用方法：</p>
              <div class="content content-4">
                <img src="@/assets/images/solution/形状8拷贝.png" alt="" />
                <span>
                  开通了本地用印权限的用户，录入指纹比对，身份验证通过后立即
                  开锁，盖印信息及盖印照片即时上传到云服务器，可供随时查看。
                </span>
              </div>
              <div class="content content-5">
                <img src="@/assets/images/solution/形状8拷贝.png" alt="" />
                <span>
                  在4G或者WIFI网络环境不佳和没有网络的情况下，本地用印模式能
                  够正常使用。用印信息和用印照片保存到便携机内存中，在连接网络
                  后会自动上传用印信息和照片到云服务器，可供随时查看。
                </span>
              </div>
              <div class="content content-3">
                <img src="@/assets/images/solution/形状8拷贝.png" alt="" />
                <span> 开锁时间 0.2秒 </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="view10">
      <div class="view10-warp">
        <p class="p-1">印章换印操作步骤</p>
        <div class="icon-1">
          <img src="@/assets/images/solution/内容.png" alt="" />
        </div>
        <p class="p-2">
          印章套件与智能印章设备采用分离式设计，装上或取下7秒内即可完成，易用的同时保证了使用的安全性。
        </p>
        <div class="img-1">
          <img src="@/assets/images/solution/步骤内容.png" alt="" />
        </div>

        <p class="p-1">印章换印操作步骤</p>
        <div class="icon-2">
          <img src="@/assets/images/solution/内容.png" alt="" />
        </div>
        <div class="img-2">
          <img src="@/assets/images/solution/第五级盖印步骤.png" alt="" />
        </div>
        <div class="img-3">
          <img src="@/assets/images/solution/组65.png" alt="" />
        </div>
      </div>
    </div>

    <div class="view3 view11">
      <div class="view3-warp view11-warp">
        <p class="title-1">智能AI印控台</p>
        <!-- <div class="icon"> -->
        <img src="@/assets/images/solution/内容.png" alt="" />
        <!-- </div> -->
        <div class="view3-warp-box view11-warp-box">
          <div class="left-box box">
            <div>
              <img src="@/assets/images/solution/头图2.png" alt="" />
            </div>
          </div>
          <div class="right-box box">
            <div class="head">设备性能参数</div>
            <div class="item">
              <div class="item-left">额定电压频率： DC12 3A</div>
              <div class="item-right">机身尺寸（直径×高）： 332*306*160mm</div>
            </div>
            <div class="item">
              <div class="item-left">重量：3.28kg</div>
              <div class="item-right">
                安全识别： 指纹/人脸/账号密码/二维码登录
              </div>
            </div>
            <div class="item">
              <div class="item-left">网络： WiFi/5G/有线（外设）</div>
              <div class="item-right">工作温度： -10℃+40℃</div>
            </div>
            <div class="item">
              <div class="item-left">摄像头：3个（500万像素）</div>
              <div class="item-right">材质： 铝合金壳体一次性冲压成型</div>
            </div>
            <div class="item">
              <div class="item-left">屏幕尺寸： 10.1寸</div>
              <div class="item-right">
                盖印安全： 电子感应围栏，用印文件二次采集
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="view12">
      <div class="view12-warp">
        <p class="p-1">用印设备盖章与实际用印文件一致性</p>
        <div class="icon-2">
          <img src="@/assets/images/solution/内容.png" alt="" />
        </div>
        <p class="p-2">
          智能AI印控台配备了3个500万像素高清摄像头，在盖印前期印控台可通过人脸识别、指纹识别、扫描二维码以及账号密码多方式登录，在盖印过程智能AI印控台会通过红外感应锁定用印文件，同时智能AI印控台盖完印后会立即将盖章信息和盖章后的照片上传到云服务器，盖印和拍照动作全自动完成。盖印完成后用户可以通过后台记录对盖印图片与真实文件做对比。
        </p>
        <!-- <p class="p-3">台会通过红外感应锁定用印文件，同时智能AI印控台盖完印后会立即将盖章信息和盖章后的照片上传到云服务器，盖印和拍照动作全自动完成。盖印完成后用</p> -->
        <!-- <p class="p-4"></p> -->
        <div class="img">
          <img src="@/assets/images/solution/组67.png" alt="" />
        </div>
      </div>
    </div>

    <div class="view13">
      <div class="view13-warp">
        <p class="title-1">智能AI印控台结构图</p>
        <p class="title-2">
          智能AI印控台外壳使用铝合金壳体一次性冲压成型，防拆防爆。红外电子围栏感应限定盖章范围，避免乱盖、误盖。
        </p>
        <div class="img">
          <img
            src="@/assets/images/solution/印控台设备结构图.png"
            alt=""
            srcset=""
          />
        </div>
      </div>
    </div>

    <div class="view14">
      <div class="view14-warp">
        <p class="p-1">质量证书</p>
        <div class="icon">
          <img src="@/assets/images/solution/内容.png" alt="" />
        </div>
        <div class="img">
          <img src="@/assets/images/solution/组74.png" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "solution",
  data() {
    return {
      tableData: [
        {
          type: "光敏印章",
        },
        {
          type: "红胶印章",
        },
        {
          type: "铜质印章",
        },
        {
          type: "原子印章",
        },
        {
          type: "回墨印章",
        },
        {
          type: "日期印章",
        },
        {
          type: "...",
        },
        {
          type: "尺寸大小",
        },
      ],
    };
  },
  mounted() {},
  computed: {},
  watch: {},
  methods: {},
};
</script>
<style lang="scss" scoped>
.solution-page {
  width: 1920px;
  .view {
    width: 100%;
    height: 360px;
    background: #050b19;
    overflow: hidden;
    &-warp {
      width: 100%;
      height: 100%;
      &-box {
        display: flex;
        align-items: center;
        justify-content: center;
        margin-left: 300px;
        .left-box {
          .text-1 {
            font-size: 36px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #ffffff;
          }
          .text-2 {
            width: 589px;
            height: 38px;
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #ffffff;
            line-height: 23px;
            margin: 39px 0 47px;
          }
          .btn {
            width: 106px;
            height: 32px;
            background: #d51515;
            text-align: center;
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #ffffff;
            line-height: 32px;
          }
        }
      }
    }
  }
  .view2 {
    width: 100%;
    height: 416px;
    background: #f4f7fa;
    overflow: hidden;
    &-warp {
      width: 1146px;
      margin: 0 auto;
      height: 100%;
      &-box {
        height: 100%;
        display: flex;
        align-items: center;
        margin-left: 20px;
        .left-box {
          margin-right: 189px;
          .text-1 {
            font-size: 28px;
            font-family: Microsoft YaHei;
            font-weight: bold;
            color: #010a2b;
          }
          .icon {
            margin: 21px 0 35px;
          }
          .text-2 {
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: rgba($color: #000000, $alpha: 0.9);
          }
          .text-3 {
            margin-top: 25px;
          }
        }
      }
    }
  }
  .view3 {
    width: 100%;
    height: 457px;
    background: #ffffff;
    overflow: hidden;
    &-warp {
      text-align: center;
      width: 1305px;
      height: 100%;
      margin: 0 auto;
      .title-1 {
        font-size: 28px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #010a2b;
        margin: 31px 0 0px;
      }
      .view3-warp-box {
        display: flex;
        align-items: center;
        height: 380px;
        .right-box {
          margin-left: 86px;
          .head {
            width: 522px;
            height: 40px;
            background: #de1c24;
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #ffffff;
            text-align: center;
            line-height: 40px;
          }
          .item {
            width: 522px;
            height: 40px;
            background: rgba(49, 49, 49, 0);
            box-shadow: 0px 1px 0px 0px rgba(0, 0, 0, 0.1);
            display: flex;
            align-items: center;
            // justify-content: space-between;
            font-size: 12px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #666666;
            padding: 0 16px;
            text-align: left;
            box-sizing: border-box;
            .item-left,
            .item-right {
              width: 50%;
            }
          }
        }
      }
    }
  }
  .view4 {
    width: 100%;
    height: 578px;
    background: #ffffff;
    overflow: hidden;
    &-warp {
      width: 1146px;
      margin: 0 auto;
      text-align: center;
      .title-2 {
        font-size: 26px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #000000;
        margin: 28px 0 41px;
      }
      .btn-box {
        display: flex;
        justify-content: space-around;
        height: 40px;
        width: 797px;
        margin: 0 auto;
        margin-bottom: 57px;
        .item {
          width: 225px;
          height: 100%;
          background: #de1c24;
          font-size: 18px;
          font-family: Microsoft YaHei;
          font-weight: 400;
          color: #ffffff;
          color: rgba($color: #ffffff, $alpha: 0.8);
          line-height: 40px;
        }
      }
    }
  }
  .view5 {
    width: 100%;
    height: 636px;
    background: #1c1d21;
    overflow: hidden;
    &-warp {
      width: 1146px;
      height: 100%;
      margin: 0 auto;
      text-align: center;
      overflow: hidden;
      .title {
        font-size: 26px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #ffffff;
        margin: 41px 0 58px;
      }
      .img {
        margin-left: -80px;
      }
    }
  }
  .view6 {
    width: 100%;
    height: 1030px;
    background: #fbfbfb;
    overflow: hidden;
    &-warp {
      width: 1146rpx;
      margin: 0 auto;
      text-align: center;
      .title-2 {
        font-size: 28px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #010a2b;
        margin-top: 60px;
      }
      .title-3 {
        font-size: 16px;
        width: 741px;
        height: 42px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: rgba($color: #000000, $alpha: 0.8);
        margin: 34px auto 45px;
      }
      .header {
        width: 1144px;
        height: 47px;
        background: rgba(242, 242, 242, 0);
        border: 1px solid #e8e8e8;
        font-size: 18px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: #010101;
        line-height: 47px;
        text-align: center;
        margin: 0 auto;
        margin-top: 45px;
      }
      .view6-warp-img {
        margin: 37px 0 33px;
      }
      .view6-warp-table {
        width: 1144px;
        margin: 0 auto;
        tr:last-child {
          height: 70px;
          line-height: 70px;
        }
        tr:nth-child(2n + 1) {
          background-color: #f2f2f2;
          border: 1px solid #e8e8e8;
        }
        tr {
          width: 100%;
          height: 100%;
          td {
            width: 160px;
            height: 40px;
            background: rgba(49, 49, 49, 0);
            border: 0.5px solid #e8e8e8;
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #1d1e2a;
            line-height: 40px;
            text-align: center;
          }
          .item-td-1 {
            width: 248px;
          }
        }
        .item-tr-1 {
          background: #e62129;
          td {
            background: #e62129;
            border: none;
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #ffffff;
          }
        }
      }
    }
  }
  .view7 {
    width: 100%;
    height: 970px;
    background: #f3f3f3;
    overflow: hidden;
    &-warp {
      width: 1146rpx;
      margin: 0 auto;
      text-align: center;
      .title-2 {
        font-size: 28px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #010a2b;
        margin: 60px 0 15px;
      }
      .title-3 {
        font-size: 16px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: rgba($color: #000000, $alpha: 0.8);
      }
      .header {
        width: 227px;
        height: 40px;
        background: #d63c3c;
        font-size: 18px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: #ffffff;
        line-height: 40px;
        text-align: center;
        margin: 0 auto;
        margin-top: 67px;
      }
      .view7-warp-img {
        margin: 51px 0 94px;
      }
    }
  }
  .view8 {
    width: 100%;
    height: 700px;
    overflow: hidden;
    &-warp {
      width: 1146px;
      height: 100%;
      margin: 0 auto;
      text-align: center;
      .title-1 {
        font-size: 28px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #010a2b;
        margin: 72px 0 28px;
      }
      &-box {
        display: flex;
        width: 969px;
        margin: 0 auto;
        margin-top: 86px;
        &-item {
          .container {
            display: flex;
            .xuhao {
              width: 24px;
              height: 24px;
              background: #f73131;
              border-radius: 50%;
              font-size: 18px;
              font-weight: normal;
              font-style: italic;
              color: #ffffff;
              line-height: 24px;
              text-align: center;
            }
            .title {
              font-size: 20px;
              font-family: Microsoft YaHei;
              font-weight: 400;
              color: #000000;
              margin-left: 11px;
            }
          }
          .message {
            width: 447px;
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: rgba($color: #000000, $alpha: 0.8);
            text-align: left;
            margin-top: 33px;
          }
        }
        &-left {
          margin-right: 37px;
          .img {
            margin-top: 65px;
          }
        }
        &-right {
          .img {
            margin-left: 31px;
            margin-bottom: 10px;
          }
        }
      }
    }
  }
  .view9 {
    width: 100%;
    overflow: hidden;
    &-warp {
      width: 100%;
      height: 100%;
      text-align: center;
      .title-1 {
        font-size: 28px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #010a2b;
        margin-top: 35px;
      }
      .img {
        margin: 38px 0 42px;
      }
      &-model {
        width: 100%;
        height: 350px;
        background: #ce2526;
        &-box {
          display: flex;
          width: 995px;
          height: 100%;
          margin: 0 auto;
        }
        .model-item {
          text-align: left;
          .p-1 {
            font-size: 22px;
            font-family: Microsoft YaHei;
            font-weight: bold;
            color: #ffffff;
            margin-top: 40px;
          }
          .p-2 {
            font-size: 16px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: rgba($color: #ffffff, $alpha: 0.7);
            margin: 40px 0 19px;
          }
          .content-1 {
            width: 409px;
            height: 40px;
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #ffffff;
          }
          .content-2 {
            width: 424px;
            height: 40px;
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #ffffff;
            margin: 32px 0 35px;
          }
          .content-3 {
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #ffffff;
          }
          .content-4 {
            width: 405px;
            height: 40px;
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #ffffff;
            margin: 32px 0 30px;
          }
          .content-5 {
            width: 421px;
            height: 66px;
            font-size: 14px;
            font-family: Microsoft YaHei;
            font-weight: 400;
            color: #ffffff;
          }
        }
        .model-left {
          width: 50%;
          border-right: 1px solid #f25a5b;
        }
        .model-right {
          width: 50%;
          padding-left: 60px;
          box-sizing: border-box;
        }
      }
    }
  }
  .view10 {
    width: 100%;
    height: 1656px;
    overflow: hidden;
    &-warp {
      width: 1146px;
      margin: 0 auto;
      text-align: center;
      .p-1 {
        font-size: 28px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #010a2b;
        margin: 66px 0 25px;
      }
      .p-2 {
        font-size: 16px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: rgba($color: #000000, $alpha: 0.8);
        margin: 58px 0 35px;
      }
      .icon-2 {
        margin-bottom: 25px;
      }
      .img-2 {
        margin-bottom: 25px;
      }
    }
  }
  .view11 {
    width: 100%;
    height: 430px;
    background: #f8f7f7;
    overflow: hidden;
    &-warp {
      &-box {
        height: auto !important;
      }
    }
  }
  .view12 {
    width: 100%;
    height: 489px;
    overflow: hidden;
    &-warp {
      width: 1146px;
      margin: 0 auto;
      text-align: center;
      .p-1 {
        font-size: 28px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #010a2b;
        margin-top: 48px;
      }
      .p-2 {
        width: 971px;
        height: 70px;
        font-size: 14px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: rgba($color: #000000, $alpha: 0.8);
        text-align: left;
        margin: 39px auto 49px;
      }
    }
  }
  .view13 {
    width: 100%;
    height: 690px;
    background: #1c1d21;
    overflow: hidden;
    &-warp {
      width: 1146px;
      margin: 0 auto;
      text-align: center;
      .title-1 {
        font-size: 26px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #ffffff;
        margin: 50px 0 30px;
      }
      .title-2 {
        font-size: 16px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        color: rgba($color: #ffffff, $alpha: 0.8);
        margin-bottom: 124px;
      }
    }
  }
  .view14 {
    width: 100%;
    height: 651px;
    overflow: hidden;
    &-warp {
      width: 1146px;
      margin: 0 auto;
      text-align: center;
      .p-1 {
        font-size: 28px;
        font-family: Microsoft YaHei;
        font-weight: bold;
        color: #010a2b;
        margin: 48px 0 10px;
      }
      .img {
        margin-top: 45px;
      }
    }
  }
}
</style>
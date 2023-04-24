<template>
  <div class="pager-container">
    <div class="img"></div>
    <div class="img-round"></div>
    <div class="img-3"></div>
    <div class="img-4"></div>
    <div class="img-5"></div>
    <div class="right-container">
      <div
        class="change-la"
        :class="isCN ? 'change-select' : 'change-unselect'"
        @click="isCN = true"
      >
        <div>{{ !isCN ? "中文" : "CN" }}</div>
      </div>
      <div
        class="change-la"
        :class="!isCN ? 'change-select' : 'change-unselect'"
        @click="isCN = false"
      >
        <div>EN</div>
      </div>
    </div>
    <div class="name">
      <div class="logo"></div>
      <div class="logo-name" v-show="isCN"><div>杭州毒鱼科技有限公司</div></div>
      <div class="des" :class="isCN ? 'des-1' : 'des-2'">
        {{ info.des }}
      </div>
      <div class="row-log">
        <div class="icon-13"></div>
        <div class="icon-12"></div>
        <div class="icon-11"></div>
      </div>
    </div>
    <div class="bottom-container">
      <div class="tel">{{ info.contact }}</div>
      <div class="mail">{{ info.mail }}</div>
      <div class="address">
        {{ info.address }}
      </div>
      <a class="bah" href="https://beian.miit.gov.cn/">浙ICP备2023003886号-1</a>
    </div>
  </div>
</template>
<script >
export default {
  data() {
    return {
      infoCN: {
        address: "地址：浙江省杭州市滨江区西兴街道聚工路11号5幢3层309室",
        mail: "邮箱：allenwithlee@126.com",
        contact: "合作请联系：Allen",
        des: "是一个致力于开发超休闲游戏，抖音、微信小游戏，VR游戏的工作团队，团队经验丰富，已有各类游戏产品数百款。",
      },
      infoEN: {
        address:
          "Address: Room 309, 3rd Floor, Building 5, No. 11, Jugong Road, Xixing Street, Binjiang District, Hangzhou City, Zhejiang Province",
        mail: "E-mail：allenwithlee@126.com",
        contact: "Contact：Allen",
        des: "We create premium games",
      },
      isCN: true,
      iconCN: new URL("@/assets/image/icon_cn.png", import.meta.url),
      iconEN: new URL("@/assets/image/icon_en.png", import.meta.url),
      iconCH: new URL("@/assets/image/icon_chease.png", import.meta.url),
    };
  },
  computed: {
    info() {
      return this.isCN ? this.infoCN : this.infoEN;
    },
  },
};
</script>
<style lang="scss">
.pager-container {
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  position: relative;
  background-color: white;

  .img {
    position: absolute;
    z-index: 1;
    right: 0;
    top: 0;
    width: 50vw;
    height: 100vh;
    background-image: url("@/assets/image/page_bg.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    object-fit: cover;
  }
  .img-round {
    position: absolute;
    z-index: 2;
    left: 50%;
    top: 0;
    width: 19.563vh;
    height: 100vh;
    background-image: url("@/assets/image/round_top.png");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }
  .img-3 {
    position: absolute;
    z-index: 3;
    left: 50%;
    top: 2vh;
    width: 25vh;
    height: 27.89vh;
    background-image: url("@/assets/image/icon_3.png");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }
  .img-4 {
    position: absolute;
    z-index: 3;
    left: calc(50% - 25vh);
    top: calc(50% - 5vh);
    transform: translateY(-50%);
    width: 25vh;
    height: 28.36vh;
    background-image: url("@/assets/image/icon_4.png");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }
  .img-5 {
    position: absolute;
    z-index: 3;
    left: calc(50% - 5vh);
    bottom: 10vh;
    width: 25vh;
    height: 28.36vh;
    background-image: url("@/assets/image/icon_5.png");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }
  .right-container {
    position: absolute;
    z-index: 3;
    right: 4vw;
    top: 2vh;
    display: flex;
    width: 50px;
    justify-content: space-between;
    align-items: center;
    .change-la {
      width: 20px;
      height: 20px;
      text-align: center;
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      color: white;

      div {
        white-space: nowrap;
        font-size: 6;
      }
    }
    .change-select {
      border: 1px solid white;
    }
    .change-unselect {
      border: 0px solid transparent;
    }
  }
  .name {
    position: absolute;
    top: 2.533vh;
    left: 1vw;
    z-index: 10;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    font-size: 12px;
    color: black;
    .logo {
      width: 40vh;
      height: 13.872vh;
      background-image: url("@/assets/image/pufferstudios.png");
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
    }
    .logo-name {
      width: 100%;
      height: 30px;
      line-height: 20px;
      padding-left: 4vh;
      background-image: url("@/assets/image/icon_1.png");
      background-size: contain;
      background-position: 0 center;
      background-repeat: no-repeat;
      display: flex;
      justify-content: flex-start;
      align-items: center;
      div {
        font-weight: 600;
      }
    }
    .des {
      margin-top: 2vw;
      width: 30vw;
      font-weight: 500;
      font-size: 9px;
    }
    .des-1 {
      font-size: 9px;
      font-weight: 600;
    }
    .des-2 {
      font-size: 18px;
      font-weight: 700;
    }
    .row-log {
      display: flex;
      margin-top: 5vh;
      width: 30vw;
      justify-content: space-between;
      font-size: 8px;
      color: coral;
      .icon-13 {
        width: 15vh;
        height: 15vh;
        background-image: url("@/assets/image/icon_13.png");
        background-size: contain;
        background-position: center;
        background-repeat: no-repeat;
        display: flex;
        flex-direction: column;
        position: relative;
      }
      .icon-12 {
        width: 15vh;
        height: 15vh;
        background-image: url("@/assets/image/icon_12.png");
        background-size: contain;
        background-position: center;
        background-repeat: no-repeat;
        position: relative;
      }
      .icon-11 {
        width: 15vh;
        height: 15vh;
        background-image: url("@/assets/image/icon_11.png");
        background-size: contain;
        background-position: center;
        background-repeat: no-repeat;
        position: relative;
      }
    }
  }
  .bottom-container {
    position: absolute;
    bottom: 1vh;
    left: 2vw;
    width: 45vw;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-size: 10px;
    color: black;
    flex-basis: 0;
    flex-wrap: wrap;
    font-family: sans-serif;
    .bah{
      font-size: 6px;
      font-weight: 300;
      white-space: nowrap;
    }
    .tel {
      padding: 3px 10px;
      background-color: rgb(254, 199, 52);
      border-radius: 10px;
      white-space: nowrap;
      font-weight: 600;
      text-align: center;
    }

    .mail {
      white-space: nowrap;
      font-weight: 600;
      text-align: center;
    }
    .address {
      width: 45vw;
      font-weight: 600;
      text-align: center;
    }
  }
}
</style>

<script setup>
</script>

<template>
  <div class="pager-container">
    <div class="img"></div>
    <div class="name">
      <div class="logo"></div>
      <div class="des">
        杭州毒鱼科技有限公司，是一个致力于开发超休闲游戏，抖音、微信小游戏，VR游戏的工作团队，团队经验丰富，已有各类游戏产品数百款。
      </div>
    </div>
    <div class="bottom-container">
      <div class="tel">合作请联系：Allen</div>
      <div class="mail">邮箱：allenwithlee@126.com</div>
      <div class="address">
        地址：浙江省杭州市滨江区西兴街道聚工路11号5幢3层309室
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.pager-container {
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  .img {
    width: 100vw;
    height: 100vh;
    background-image: url("@/assets/image/page_bg.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    position: relative;
    filter: blur(1px);
  }
  .name {
    position: absolute;
    top: 2.533vw;
    left: 5vw;
    z-index: 10;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    font-size: 12px;
    color: white;
    font-weight: 300;
    .logo {
      width: 13.333vw;
      height: 4.624vw;
      background-image: url("@/assets/image/pufferstudios.png");
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
    }
    .des {
      margin-top: 2vw;
      width: 40vw;
      font-weight: 500;
    }
  }
  .bottom-container {
    position: absolute;
    bottom: 4vw;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-size: 12px;
    color: white;
    font-weight: 300;
    flex-wrap: wrap;

    .tel {
      white-space: nowrap;
    }

    .mail {
      white-space: nowrap;
    }
    .address {
      white-space: nowrap;
    }
  }
}
</style>

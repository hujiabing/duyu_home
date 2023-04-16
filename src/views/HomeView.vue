<template>
  <div class="pager-container">
    <div class="img"></div>
    <div class="img-round"></div>
    <div class="img-3"></div>
    <div class="img-4"></div>
    <div class="img-5"></div>
    <div class="name">
      <div class="logo"></div>
      <div class="logo-name"><div>杭州毒鱼科技有限公司</div></div>
      <div class="des">
        是一个致力于开发超休闲游戏，抖音、微信小游戏，VR游戏的工作团队，团队经验丰富，已有各类游戏产品数百款。
      </div>
      <div class="row-log">
        <div class="icon-13"></div>
        <div class="icon-12"></div>
        <div class="icon-11"></div>
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
<script >
export default {};
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
      div{
        font-weight: 600;
      }
    }
    .des {
      margin-top: 2vw;
      width: 30vw;
      font-weight: 500;
      font-size: 9px;
    }
    .row-log {
      display: flex;
      margin-top: 3vh;
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
        &::after{
          position: absolute;
          left: 50%;
          transform: translateX(-50%);
          bottom: -12px;
          white-space: nowrap;
          content: "Stump Me";
        }
      }
      .icon-12 {
        width: 15vh;
        height: 15vh;
        background-image: url("@/assets/image/icon_12.png");
        background-size: contain;
        background-position: center;
        background-repeat: no-repeat;
        position: relative;
        &::after{
          position: absolute;
          left: 50%;
          transform: translateX(-50%);
          bottom: -12px;
          white-space: nowrap;
          content: "Pin Rescue";
        }
      }
      .icon-11 {
        width: 15vh;
        height: 15vh;
        background-image: url("@/assets/image/icon_11.png");
        background-size: contain;
        background-position: center;
        background-repeat: no-repeat;
        position: relative;
        &::after{
          position: absolute;
          left: 50%;
          transform: translateX(-50%);
          bottom: -12px;
          white-space: nowrap;
          content: "Spider King";
        }
      }
    }
  }
  .bottom-container {
    position: absolute;
    bottom: 4vh;
    left: 2vw;
    width: 60px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-size: 10px;
    color: black;
 
    flex-wrap: wrap;
    font-family:sans-serif;

    .tel {
      padding: 3px 10px;
      background-color: rgb(254, 199, 52);
      border-radius: 10px;
      white-space: nowrap;
      font-weight: 600;
    }

    .mail {
      white-space: nowrap;
      font-weight: 600;
    }
    .address {
      white-space: nowrap;
      font-weight: 600;
    }
  }
}
</style>

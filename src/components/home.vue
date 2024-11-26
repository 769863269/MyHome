<script setup></script>

<template>
  <!-- 左侧图片 -->
  <div class="bgBox">
    <img src="https://i.p-i.vip/43/20240915-66e6e5abe3e97.webp" />
  </div>

  <!-- 右上角格子 -->
  <div class="bgGrid">
    <div class="Grid">
      <div class="mask"></div>
      <div class="itemGrid-row" v-for="i in 9" :key="i">
        <div class="itemGrid-cols" v-for="j in 5" :key="j"></div>
      </div>
    </div>
  </div>

  <!-- 个人信息 -->
  <div class="main">
    <div class="info">
      <!-- 个人头像 -->
      <div class="header">
        <img src="../assets/user.png" />
      </div>
      <!-- 个人名称 -->
      <div class="infoText">
        <h1>Hi</h1>
        <h1>I'm <span class="nameText">KongDong</span></h1>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@media (max-width: 1100px) {
  .bgBox {
    display: none;
  }
}

.bgBox {
  position: fixed;
  bottom: 0;
  width: 400px;
  img {
    width: 100%;
    height: auto;
  }
}

.bgGrid {
  .Grid {
    display: flex;
    justify-content: flex-end;
    position: absolute;
    right: 0;
    top: 0;

    .mask {
      width: 100%;
      height: 100%;
      position: absolute;
      background-image: linear-gradient(
        to top right,
        #fff 50%,
        rgb(255 255 255 / 0) 100%
      );
    }

    .itemGrid-row {
      .itemGrid-cols {
        width: 88px;
        height: 88px;
        border-left: 1px dashed #000;
        border-bottom: 1px dashed #000;
      }
    }
  }
}

.main {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;

  .info {
    display: flex;
    z-index: 1;

    .infoText {
      display: flex;
      justify-content: center;
      align-items: start;
      flex-direction: column;
      margin-left: 20px;

      .nameText {
        position: relative;

        &::before {
          position: absolute;
          border-radius: 5px;
          bottom: 0;
          left: 50%;
          transform: translateX(-50%);
          z-index: -1;
          content: "";
          background: #fe859994;
          height: 30%;
          width: 110%;
          display: inline-block;
        }
      }
    }

    .header {
      width: 150px;
      height: 150px;
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;

      img {
        border-radius: 50%;
        width: 100%;
        height: 100%;
        border: 3px #fff solid;
        box-shadow: 0 0 15px 6px #ffb3b3;
        object-fit: cover;
      }
    }
  }
}
</style>

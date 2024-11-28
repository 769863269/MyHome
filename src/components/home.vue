<script setup>
import { ref } from "vue";

const typedStrings = ref([
  "你好鸭，欢迎来到我的主页！",
  "长风破浪会有时，直挂云帆济沧海",
  "沉舟侧畔千帆过，病树前头万木春",
  "纸上得来终觉浅，绝知此事要躬行",
  "时人不识凌云木，直待凌云始道高",
  "欲穷千里目，更上一层楼",
  "大鹏一日同风起，扶摇直上九万里",
]);
</script>

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
        <h1>I'm <span class="nameText">空洞</span></h1>
      </div>
    </div>

    <div class="typeText">
      <VueTyped
        :strings="typedStrings"
        :typeSpeed="50"
        :backSpeed="30"
        :loop="true"
      />
    </div>
  </div>
</template>

<style lang="scss" scoped>
@media screen and (max-width: 762px) {
  .bgBox {
    width: 60% !important;
    right: 62vw !important;
  }

  .bgGrid {
    .Grid {
      .itemGrid-row {
        .itemGrid-cols {
          width: 60px !important;
          height: 60px !important;
        }
      }

      .mask {
        height: 110% !important;
      }
    }
  }

  .main {
    background-size: cover !important;
    background-position: -20em !important;

    .info {
      flex-direction: column;
      align-items: center;

      .infoText {
        align-items: center !important;
        font-size: 1em !important;
        margin: 0 !important;
      }

      .header {
        margin: 0 0 1em 0;
      }
    }

    .typeText {
      margin: 20px !important;
    }
  }
}

.bgBox {
  width: 450px;
  z-index: 1;
  position: fixed;
  bottom: 0;
  left: -50px;
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
  flex-direction: column;

  .info {
    display: flex;
    z-index: 1;

    .infoText {
      display: flex;
      justify-content: center;
      align-items: start;
      flex-direction: column;
      margin-left: 30px;

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

  .typeText {
    font-size: 24px;
    margin: 50px;

    z-index: 1;
    display: flex;
    height: 50px;
    text-align: center;
  }
}
</style>

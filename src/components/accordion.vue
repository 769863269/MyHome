<script setup></script>

<template>
  <div class="warpper">
    <div class="buttons">
      <div class="icon">
        <i class="fa fa-facebook" aria-hidden="true" />
      </div>
      <span>facebook</span>
    </div>
    <div class="buttons">
      <div class="icon">
        <i class="fa fa-twitter" aria-hidden="true" />
      </div>
      <span>twitter</span>
    </div>
    <div class="buttons">
      <div class="icon">
        <i class="fa fa-github" aria-hidden="true" />
      </div>
      <span>github</span>
    </div>
    <div class="buttons">
      <div class="icon">
        <i class="fa fa-wechat" aria-hidden="true" />
      </div>
      <span>wechat</span>
    </div>
    <div class="buttons">
      <div class="icon">
        <i class="fa fa-qq" aria-hidden="true" />
      </div>
      <span>腾讯QQ</span>
    </div>
    <div class="buttons">
      <div class="icon">
        <i class="fa fa-weibo" aria-hidden="true" />
      </div>
      <span>微博</span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@media screen and (min-width: 930px) {
  .warpper .buttons {
    width: 60px !important;
    height: 60px !important;
    border-radius: 60px !important;
    margin: 0 10px !important;
    box-shadow: 4px 12px 9px rgba(0, 0, 0, 0.07) !important;
  }
  .warpper .buttons:hover {
    width: 280px !important;
  }
  .warpper .buttons .icon {
    width: 60px !important;
    height: 60px !important;
    border-radius: 60px !important;
    font-size: 38px !important;
  }
  .warpper .buttons span {
    font-size: 32px !important;
  }
}

.warpper {
  display: flex;
}

.warpper .buttons {
  width: 38px;
  height: 38px;
  border-radius: 38px;
  margin: 0 3px;
  overflow: hidden;
  background: #fff;
  cursor: pointer;
  box-shadow: 4px 6px 9px rgba(0, 0, 0, 0.07);
  transition: all 0.3s;
}

.warpper .buttons:hover {
  width: 150px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.warpper .buttons .icon {
  width: 38px;
  height: 38px;
  border-radius: 38px;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: all 0.3s;
  font-size: 26px;
}

.warpper .buttons:nth-child(1):hover .icon {
  background: #4267b2;
  color: #fff;
}
.warpper .buttons:nth-child(2):hover .icon {
  background: #1da1f2;
  color: #fff;
}
.warpper .buttons:nth-child(3):hover .icon {
  background: #333;
  color: #fff;
}
.warpper .buttons:nth-child(4):hover .icon {
  background: #00b8a9;
  color: #fff;
}
.warpper .buttons:nth-child(5):hover .icon {
  background: #f6416c;
  color: #fff;
}
.warpper .buttons:nth-child(6):hover .icon {
  background: #ffde7d;
  color: #fff;
}

.warpper .buttons:hover .icon {
  transition: all 0.5s;
}

.warpper .buttons span {
  flex: 2;
  text-align: center;
  font-size: 22px;
  opacity: 0;
  transition: all 0.5s;
}

.warpper .buttons:hover span {
  opacity: 1;
}
</style>

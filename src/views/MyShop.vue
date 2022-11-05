<template>
  <div class="container">
    <div class="content">
      <div class="header">
        <img src="@/assets/images/header-image.webp" alt="" />
        <a href="#">请登录</a>
      </div>
      <div class="main">
        <div class="balance main-style">
          <div class="balance-left">
            <i>￥0</i>
            <b>余额</b>
          </div>
          <div class="balance-line"></div>
          <div class="balance-right">
            <i>0</i>
            <b>优惠券</b>
          </div>
        </div>
        <div class="order main-style">2</div>
        <div class="service main-style">3</div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
/* header */
.header {
  width: 100%;
  background-image: url("../assets/images/background.png");
  background-repeat: no-repeat;
  height: 170px;
  text-align: center;
}

.header img {
  margin-top: 30px;
  width: 70px;
  border-radius: 50%;
}
.header a {
  display: block;
  color: #fff;
  margin: 5px 0;
}

/* main */
.main {
  margin-top: -30px;
}
.main-style {
  border-radius: 10px;
  width: 90%;
  background-color: #fff;
  box-shadow: 0 1px 5px 0 #f1f1f1;
  margin: 5px auto;
}
.balance {
  display: flex;
  justify-content: space-around;
  padding: 20px 0;
}
.balance-left,
.balance-right {
  flex: 0 1 49%;
  text-align: center;
  display: flex;
  flex-direction: column;
}
.balance-line {
  background-color: #ebebeb;
  flex: 0 1 1px;
  margin: 5px 0;
}
.balance-left i,
.balance-right i {
  font-size: 18px;
  margin: 10px 0;
}
.balance-left b,
.balance-right b {
  color: #9b9b9b;
  font-weight: 400;
}
</style>

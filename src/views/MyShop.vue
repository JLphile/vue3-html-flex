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
        <div class="order main-style">
          <div class="order-text">
            <h4>我的订单</h4>
            <a href="#">全部订单></a>
          </div>
          <ul>
            <li>
              <a href="#">
                <i class="icon-fenlei"></i>
                <span>待发货</span>
              </a>
            </li>
            <li>
              <a href="#">
                <i class="icon-fenlei"></i>
                <span>配送中</span>
              </a>
            </li>
            <li>
              <a href="#">
                <i class="icon-fenlei"></i>
                <span>待提货</span>
              </a>
            </li>
            <li>
              <a href="#">
                <i class="icon-fenlei"></i>
                <span>售后服务</span>
              </a>
            </li>
          </ul>
        </div>
        <div class="service main-style">
          <h4>我的服务</h4>
          <ul>
            <li>
              <a href="#">
                <i class="icon-fenlei"></i>
                <span>快速核销</span>
              </a>
            </li>
            <li>
              <a href="#">
                <i class="icon-fenlei"></i>
                <span>快速核销</span>
              </a>
            </li>
            <li>
              <a href="#">
                <i class="icon-fenlei"></i>
                <span>快速核销</span>
              </a>
            </li>
            <li>
              <a href="#">
                <i class="icon-fenlei"></i>
                <span>快速核销</span>
              </a>
            </li>
            <li>
              <a href="#">
                <i class="icon-fenlei"></i>
                <span>快速核销</span>
              </a>
            </li>
            <li>
              <a href="#">
                <i class="icon-fenlei"></i>
                <span>快速核销</span>
              </a>
            </li>
            <li>
              <a href="#">
                <i class="icon-fenlei"></i>
                <span>快速核销</span>
              </a>
            </li>
            <li>
              <a href="#">
                <i class="icon-fenlei"></i>
                <span>快速核销</span>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="placeholder"></div>
    <div class="footer">
      <div class="footer-lists">
        <ul>
          <li>
            <a href="#" >
              <i class="icon-shouye"></i>
              <p>首页</p>
            </a>
          </li>
          <li>
            <a href="#">
              <i class="icon-fenlei"></i>
              <p>分类</p>
            </a>
          </li>
          <li>
            <a href="#">
              <i class="icon-shouye"></i>
              <p>购物车</p>
              <b>2</b>
            </a>
          </li>
          <li>
            <a href="#" class="selected">
              <i class="icon-wode"></i>
              <p>我的</p>
            </a>
          </li>
        </ul>
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
  min-height: calc(100vh);
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
.order-text {
  display: flex;
  justify-content: space-between;
  padding: 15px 10px;
}
.order-text h4 {
  font-size: 16px;
}
.order-text a {
  color: #9b9b9b;
}
.order ul {
  display: flex;
  justify-content: space-around;
  text-align: center;
}
.order ul span {
  display: block;
}
.order ul li {
  margin: 10px 0;
}
.order ul i {
  font-size: 30px;
}
.order ul span {
  margin: 5px 0;
}
.service ul {
  display: flex;
  flex-wrap: wrap;
  text-align: center;
}
.service li {
  flex: 0 1 25%;
  margin: 5px 0;
}
.service ul span {
  display: block;
  margin: 15px 0;
}
.service h4 {
  font-size: 16px;
  padding: 15px 10px;
}
.service li i{
  font-size: 30px;
  color: #fff;
  border-radius: 50%;
  padding: 8px;
  background-color: #48befd;
}

/* 底部 */
.placeholder {
  height: 55px;
}
.footer {
  position: fixed;
  bottom: 0;
  left: 0;
  height: 55px;
  width: 100%;
}
.footer-lists {
  height: 55px;
  max-width: 720px;
  background-color: #f3f3f3;
  margin: auto;
  border-top: 1px solid #d5d5d5;
}
.footer ul {
  display: flex;
  height: 55px;
  text-align: center;
  align-items: center;
}
.footer ul li {
  flex: 0 1 25%;
}
.footer ul i {
  font-size: 24px;
}
.selected {
  color: red;
}
.footer-lists li a {
  position: relative;
}
.footer-lists li b {
  position: absolute;
  top: -13px;
  left: 13px;
  right: auto;
  background-color: #fe4557;
  color: #fff;
  border-radius: 50%;
  padding: 1px 5px;
  transform: scale(0.8);
  font-weight: 400;
}
</style>

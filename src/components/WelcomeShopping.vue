<template>
  <div class="container">
    <!-- 页面头部 -->
    <div class="index-header">
      <i class="icon-shouye"></i>
      <span>当前门店</span>
      <a href="">武汉关谷店></a>
    </div>
    <!-- 搜索栏 -->
    <div class="index-search">
      <input type="text" placeholder="请输入用户名" />
      <div class="search-item">
        <i class="icon-shouye"></i>
        <p>快速核销</p>
      </div>
    </div>
    <!-- 广告轮播 -->
    <div class="index-banner">
      <img src="@/assets/images/banner3.jpg" alt="" />
      <ul>
        <li>1</li>
        <li>/</li>
        <li>3</li>
      </ul>
    </div>
    <!-- 导航栏 -->
    <div class="index-nav">
      <ul>
        <li>
          <a href="">
            <div>新品</div>
            <p>新品专区</p>
          </a>
        </li>
        <li>
          <a href="">
            <div>新品</div>
            <p>新品专区</p>
          </a>
        </li>
        <li>
          <a href="">
            <div>新品</div>
            <p>新品专区</p>
          </a>
        </li>
        <li>
          <a href="">
            <div>新品</div>
            <p>新品专区</p>
          </a>
        </li>
        <li>
          <a href="">
            <div>新品</div>
            <p>新品专区</p>
          </a>
        </li>
        <li>
          <a href="">
            <div>新品</div>
            <p>新品专区</p>
          </a>
        </li>
        <li>
          <a href="">
            <div>新品</div>
            <p>新品专区</p>
          </a>
        </li>
        <li>
          <a href="">
            <div>新品</div>
            <p>新品专区</p>
          </a>
        </li>
      </ul>
    </div>
    <!-- 秒杀 -->
    <div class="index-seckill">
      <div class="seckill-count">
        <i class="icon-shouye"></i>
        <span>限时秒杀</span>
      </div>
      <div class="seckill-time">
        <ul>
          <li>
            <p>0:00</p>
            <b>抢购中</b>
          </li>
          <li>
            <p>10:00</p>
            <b>抢购中</b>
          </li>
          <li>
            <p>14:00</p>
            <b>抢购中</b>
          </li>
        </ul>
      </div>
      <div class="seckill-column">
        <div class="column-left">
          <a href="#">
            <img src="@/assets/images/seckill.png" alt="" />
            <span>秒杀</span>
          </a>
        </div>
        <div class="column-right">
          <h5><a href="#">农家养土鸡蛋现捡新鲜谷物虫草柴鸡蛋盒装 30枚装</a></h5>
          <p>秒杀价</p>
          <div class="column-list">
            <i>￥</i>
            <b>23.9</b>
            <s>￥44.9</s>
            <a href="#">立即抢购</a>
          </div>
        </div>
      </div>
    </div>
    <!-- 商品展示区 -->
    <div class="index-main"></div>
    <!-- 页面底部 -->
    <div class="footer"></div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
/* 首页 */
.index-header {
  margin: 5px 0;
}
.index-header i {
  color: red;
  font-size: 700;
}
/* 搜索栏 */
.index-search {
  display: flex;
  width: 100%;
  margin: 5px;
}
.index-search input {
  flex: 0 1 75%;
  background-color: #f7f7f7;
  border: 0;
  border-radius: 10px;
  outline: none;
  padding-left: 20px;
}
.search-item {
  flex: 0 1 25%;
  text-align: center;
}
/* 广告轮播 */
.index-banner {
  width: 100%;
  position: relative;
}
.index-banner img {
  width: 100%;
  border-radius: 10px;
}
.index-banner ul {
  display: flex;
  position: absolute;
  bottom: 10px;
  right: 20px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 7px;
  padding: 0 5px;
}
.index-banner ul li {
  color: #fff;
  margin: 0 1px;
}
/* 导航栏 */
.index-nav {
  width: 100%;
}
.index-nav a div {
  background: url(@/assets/images/bgc.png) no-repeat center top;
  width: 100%;
  height: 66px;
  color: #fff;
  line-height: 50px;
}
.index-nav ul {
  display: flex;
  flex-wrap: wrap;
  text-align: center;
}
.index-nav ul li {
  flex: 0 1 25%;
  margin-bottom: 10px;
}
/* 秒杀 */
.index-seckill {
  background-color: #fe6b38;
  border-radius: 10px;
  margin: 10px 0;
  padding-bottom: 10px;
}
.seckill-count {
  background-color: #fce5c6;
  width: 25%;
  border-top-left-radius: 10px;
  padding: 5px;
  color: #fe6b38;
  font-size: 14px;
}
.seckill-time ul {
  display: flex;
  text-align: center;
  margin: 10px 10px 0 10px;
}
.seckill-time ul li {
  flex: 0 1 23%;
  padding: 10px 0;
}
.seckill-time ul li p {
  color: #fff;
  font-size: 18px;
}
.seckill-time ul li b {
  color: #fff;
  font-weight: 400;
}
.seckill-time ul li:hover {
  background-color: #faa73f;
  /* border-top-left-radius: 8px; */
  /* border-top-right-radius: 8px; */
  border-radius: 8px 8px 0 0;
}
.seckill-time ul li:hover b {
  background-color: #fff;
  color: red;
  border-radius: 7px;
  padding: 0 5px;
}
.seckill-column {
  display: flex;
  background-color: #fff;
  border: 5px solid #fef9ec;
  border-radius: 8px;
  margin: 0 10px;
}
.column-left img {
  max-height: 100px;
}
.column-left {
  position: relative;
  flex: 1;
}
.column-left span {
  position: absolute;
  top: 2px;
  left: 1px;
  background-color: #fd9639;
  color: #fff;
  padding: 0 5px;
}
.column-right {
  flex: 2;
}
.column-right h5 {
  font-size: 16px;
}
.column-right h5 a {
  color: black;
}
.column-right p {
  background-color: #fd9639;
  color: #fff;
  width: 42px;
  text-align: center;
  margin-top: 15px;
}
.column-list {
  position: relative;
}
.column-list i {
  font-style: normal;
  color: #fe4557;
}
.column-list b {
  color: #fe4557;
  font-size: 18px;
  margin-left: -3px;
}
.column-list s {
  color: #999;
}
.column-list a {
  background-color: #fe4557;
  color: #fff;
  border-radius: 15px;
  padding: 4px 15px;
  font-size: 16px;
  font-weight: 700px;
  position: absolute;
  right: 0;
  bottom: 4px;
}
</style>

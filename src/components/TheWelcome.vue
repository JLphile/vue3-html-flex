<template>
  <div>
    <div class="container">
      <!-- 页面头部 -->
      <header>
        <div class="search">
          <i class="icon-qiandao"></i>
          <input type="text" placeholder="请输入商品名称" />
        </div>
      </header>
      <!-- 中间部分 -->
      <section>
        <!-- 广告图 -->
        <div class="draw">
          <img src="@/assets/images/banner.png" />
        </div>
        <!-- 轮播图 -->
        <div class="banner">
          <img src="@/assets/images/banner1.jpg" />
          <ul>
            <li></li>
            <li></li>
            <li></li>
          </ul>
        </div>

        <div class="card">
          <div class="bg-color">
            <i class="icon-libao"></i>
            <span>新客礼包</span>
          </div>
          <div class="bg-color">
            <i class="icon-libao"></i>
            <span>优惠券</span>
          </div>
          <div class="bg-color">
            <i class="icon-libao"></i>
            <span>福币兑换</span>
          </div>
          <div class="bg-color">
            <i class="icon-libao"></i>
            <span>特色商品</span>
          </div>
        </div>
        <!-- 导航栏 -->
        <div class="nav">
          <ul>
            <li>女装</li>
            <li>男装</li>
            <li>童装</li>
            <li>鞋子</li>
            <li>包包</li>
            <li>玩具</li>
          </ul>
        </div>
        <!-- 商品展示区 -->
        <div class="content">
          <div class="content-item">
            <div class="content-img">
              <img src="@/assets/images/content1.webp" alt="" />
            </div>
            <div class="content-title">
              <h5>雪纺连衣裙秋季装2021年早秋新款甜美连衣裙</h5>
            </div>
            <div class="content-box">
              <b>￥239</b>
              <span>已售出345件</span>
            </div>
          </div>
          <div class="content-item">
            <div class="content-img">
              <img src="@/assets/images/content2.webp" alt="" />
            </div>
            <div class="content-title">
              <h5>雪纺连衣裙秋季装2021年早秋新款甜美连衣裙</h5>
            </div>
            <div class="content-box"><b>￥239</b><span>已售出345件</span></div>
          </div>
          <div class="content-item">
            <div class="content-img">
              <img src="@/assets/images/content3.webp" alt="" />
            </div>
            <div class="content-title">
              <h5>雪纺连衣裙秋季装2021年早秋新款甜美连衣裙</h5>
            </div>
            <div class="content-box"><b>￥239</b><span>已售出345件</span></div>
          </div>
          <div class="content-item">
            <div class="content-img">
              <img src="@/assets/images/content4.webp" alt="" />
            </div>
            <div class="content-title">
              <h5>雪纺连衣裙秋季装2021年早秋新款甜美连衣裙</h5>
            </div>
            <div class="content-box"><b>￥239</b><span>已售出345件</span></div>
          </div>
          <div class="content-item">
            <div class="content-img">
              <img src="@/assets/images/content4.webp" alt="" />
            </div>
            <div class="content-title">
              <h5>雪纺连衣裙秋季装2021年早秋新款甜美连衣裙</h5>
            </div>
            <div class="content-box"><b>￥239</b><span>已售出345件</span></div>
          </div>
          <div class="content-item">
            <div class="content-img">
              <img src="@/assets/images/content4.webp" alt="" />
            </div>
            <div class="content-title">
              <h5>雪纺连衣裙秋季装2021年早秋新款甜美连衣裙</h5>
            </div>
            <div class="content-box"><b>￥239</b><span>已售出345件</span></div>
          </div>
        </div>
      </section>
      <!-- 底部部分 -->
      <footer>
        <div class="footer">
          <ul>
            <li>
              <a href="">
                <i class="icon-shouye"></i>
                <span>首页</span>
              </a>
            </li>
            <li>
              <a href="">
                <i class="icon-fenlei"></i>
                <span>分类</span>
              </a>
            </li>
            <li>
              <a class="select" href="">
                <i class="icon--yuan"></i>
                <span>9.9包邮</span>
              </a>
            </li>
            <li>
              <a href="">
                <i class="icon-gouwuche"></i>
                <span>购物车</span>
              </a>
            </li>
            <li>
              <a href="">
                <i class="icon-wode"></i>
                <span>我的</span>
              </a>
            </li>
          </ul>
        </div>
      </footer>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
@import "@/assets/iconfont.css";
.container {
  display: flex;
  flex-direction: column;
}
/* 头部 */
header {
  height: 5rem;
}
.search {
  position: fixed;
  z-index: 999;
  width: 100%;
  max-width: 720px;
  background-color: #fb3950;
  border-radius: 0 0 1rem 1rem;
  padding: 1rem 0;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.search i {
  color: #fff;
  margin-left: 0.5rem;
  font-size: 2.5rem;
}
.search input {
  flex: 1;
  border-radius: 1rem;
  padding: 0.5rem 0;
  margin: 0 1rem;
  text-align: center;
  color: #777;
  border: none;
}
/* 中间部分开始 */
section {
  padding: 1rem;
  /* background-color: pink; */
}
/* 广告图 */
.draw img {
  width: 100%;
  border-radius: 6rem;
}
.banner img {
  width: 100%;
  /* height: 100%; */
}
.banner {
  position: relative;
}
.banner ul {
  display: flex;
  position: absolute;
  bottom: 5px;
  left: 0;
  width: 100%;
  justify-content: center;
}
.banner ul li {
  background-color: #fff;
  margin: 5px;
  padding: 4px;
  border-radius: 50%;
}
.card {
  display: flex;
  margin: 10px 0;
  text-align: center;
}
.bg-color {
  flex: 1;
  /* background-color: pink; */
  margin: 0 3px;
  padding: 6px 0;
  border-radius: 3px;
  /* 盒子阴影 */
  box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.3);
  /* background: linear-gradient(#e8c1a6, #e98f85); */
  color: #fff;
}
.card .bg-color:nth-child(1) {
  background: linear-gradient(#e8c1a6, #e98f85);
}
.card .bg-color:nth-child(2) {
  background: linear-gradient(#e9a5ca, #ec8ab0);
}
.card .bg-color:nth-child(3) {
  background: linear-gradient(#eeb3ae, #f58695);
}
.card .bg-color:nth-child(4) {
  background: linear-gradient(#d4bbf2, #b19bf5);
}
.nav ul {
  display: flex;
  text-align: center;
}
.nav ul li {
  flex: 1;
  margin: 0 3px;
}
/* 图片展示区 */
.content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.content-item {
  flex: 0 1 49%;
  box-shadow: 0 3px 3px 0 rgba(0, 0, 0, 0.1);
  margin: 5px 0;
}
.content-img {
  width: 100%;
  height: auto;
}
.content-img img {
  max-width: 100%;
  border-radius: 5px;
  height: 100%;
}
.content-title h5 {
  font-weight: 400;
  margin: 3px;
}
.content-box {
  display: flex;
  justify-content: space-between;
  margin: 10px 0;
  padding: 0 5px;
}
.content-box b {
  color: red;
  font-size: 1.6rem;
}
.content-box span {
  color: #999;
}
/* 页面底部 */
footer {
  height: 5.5rem;
}
.footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  max-width: 72rem;
  height: 5.5rem;
  background-color: #fff;
  border-top: 1px solid #999;
}
.footer ul {
  display: flex;
  justify-content: space-around;
  align-items: center;
  height: 100%;
}
.footer ul li {
  flex: 1;
  text-align: center;
}
.footer ul li span {
  display: block;
}
.footer ul li i {
  font-size: 2rem;
}
.footer .select {
  color: red;
}
</style>

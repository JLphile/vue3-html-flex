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
            <div class="content-title">标题</div>
            <div class="content-box">单价 数量</div>
          </div>
          <div class="content-item">
            <div class="content-img">
              <img src="@/assets/images/content2.webp" alt="" />
            </div>
            <div class="content-title">标题</div>
            <div class="content-box">单价 数量</div>
          </div>
          <div class="content-item">
            <div class="content-img">
              <img src="@/assets/images/content3.webp" alt="" />
            </div>
            <div class="content-title">标题</div>
            <div class="content-box">单价 数量</div>
          </div>
          <div class="content-item">
            <div class="content-img">
              <img src="@/assets/images/content4.webp" alt="" />
            </div>
            <div class="content-title">标题</div>
            <div class="content-box">单价 数量</div>
          </div>
        </div>
      </section>
      <!-- 底部部分 -->
      <footer></footer>
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
.search {
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
  background-color: #fff;
  box-shadow: 0 3px 3px 0 rgba(0, 0, 0, 0.1);
  margin: 5px 0;
}
.content-img {
  width: 100%;
  height: 20rem;
}
.content-img img {
  max-width: 100%;
  border-radius: 5px;
  height: 100%;
}
</style>

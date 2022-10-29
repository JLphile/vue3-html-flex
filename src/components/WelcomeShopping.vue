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
    <div class="index-nav"></div>
    <!-- 秒杀 -->
    <div class="index-seckill"></div>
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
</style>

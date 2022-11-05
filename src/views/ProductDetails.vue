<template>
  <div class="container">
    <h3>商品详情</h3>
    <div class="other-header">
      <img src="@/assets/images/product1.jpg" alt="" />
    </div>
    <div class="other-time">
      <div class="time-amount">
        <i>￥</i>
        <b>23.9</b>
      </div>
      <div class="time-surplus">
        <h5>距离活动结束剩余</h5>
        <ul>
          <li class="shape">13</li>
          <li>:</li>
          <li class="shape">45</li>
          <li>:</li>
          <li class="shape">23</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.container h3 {
  padding: 5px;
}
.other-header {
  text-align: center;
}
img {
  height: 300px;
}
.other-time {
  position: relative;
  display: flex;
  max-width: 720px;
  background-color: #fa1840;
  margin-top: -30px;
  justify-content: space-between;
  padding: 5px 0;
}
.time-amount {
  display: flex;
  align-items: center;
  margin-left: 5px;
}
.time-amount i,
.time-amount b {
  color: #fff;
}
.time-amount i {
  font-style: normal;
}
.time-amount b {
  font-size: 26px;
  font-weight: 400;
  margin-left: -2px;
}
.time-surplus {
  margin-right: 5px;
  text-align: center;
}
.time-surplus ul {
  display: flex;
}
.time-surplus ul li {
  color: #fff;
  font-size: 14px;
}
.shape {
  background-color: #333;
  border-radius: 3px;
  padding: 2px;
  margin: 0 3px;
}
.time-surplus h5 {
  font-size: 14px;
  margin-bottom: 6px;
}
</style>

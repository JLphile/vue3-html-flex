<template>
  <div class="box1">
    <div>a</div>
    <div>b</div>
    <div>c</div>
    <div>d</div>
  </div>
  <div class="box2"></div>
  <div class="box3"></div>
</template>

<script setup lang="ts"></script>

<style scoped>
.box1 {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  /* justify-content: center; */
  flex-wrap: wrap;
  background-color: cyan;
  width: 600px;
  height: 600px;
}
.box1 div {
  width: 100px;
  height: 100px;
  background-color: pink;
  border: 1px solid #000;
  box-sizing: border-box;
}
</style>

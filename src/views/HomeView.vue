<template>
  <div class="home-view">
    <div>
      <CircleLoading></CircleLoading>
    </div>
  </div>
</template>

<script setup lang="ts">
import CircleLoading from "@/components/CircleLoading.vue";
</script>

<style scoped>
.home-view {
  box-sizing: content-box;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(3, 1fr);
  height: 100vh;
  justify-items: center;
  align-items: center;
  max-width: 800px;
  margin: 0 auto;
}
.home-view > div {
  transform: scale(1.5);
}
</style>

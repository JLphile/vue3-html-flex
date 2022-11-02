<template>
  <div class="home-view">
    <div>
      <CircleLoading />
    </div>
    <div>
      <BubbleLoading />
    </div>
    <div>
      <TeacupLoading />
    </div>
    <div>
      <PlayButton />
    </div>
    <div>
      <FloatingButton />
    </div>
  </div>
</template>

<script setup lang="ts">
import CircleLoading from "@/components/CircleLoading.vue";
import BubbleLoading from "@/components/BubbleLoading.vue";
import TeacupLoading from "@/components/TeacupLoading.vue";
import PlayButton from "@/components/PlayButton.vue";
import FloatingButton from "@/components/FloatingButton.vue";
</script>

<style scoped>
.home-view {
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

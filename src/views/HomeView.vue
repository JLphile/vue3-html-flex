<template>
  <div class="home-view">
    <div><CircleLoading /></div>

    <div><BubbleLoading /></div>

    <div><TeacupLoading /></div>

    <div><PlayButton /></div>

    <div><FloatingButton /></div>

    <div><ProgressBar /></div>

    <div><BadgeVue /></div>

    <div><LandMark /></div>

    <div><Heart /></div>

    <div><MailVue /></div>

    <div><CalendarVue /></div>

    <div><VueLogo /></div>
  </div>
</template>

<script setup lang="ts">
import CircleLoading from "@/components/CircleLoading.vue";
import BubbleLoading from "@/components/BubbleLoading.vue";
import TeacupLoading from "@/components/TeacupLoading.vue";
import PlayButton from "@/components/PlayButton.vue";
import FloatingButton from "@/components/FloatingButton.vue";
import ProgressBar from "@/components/ProgressBar.vue";
import BadgeVue from "@/components/BadgeVue.vue";
import LandMark from "@/components/LandMark.vue";
import Heart from "@/components/HeartVue.vue";
import MailVue from "@/components/MailVue.vue";
import CalendarVue from "@/components/CalendarVue.vue";
import VueLogo from "@/components/VueLogo.vue";
</script>

<style scoped>
.home-view {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(6, 1fr);
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

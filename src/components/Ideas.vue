<template>
  <div class="ideas">
    <HeroInformation
      title="It started with a small idea"
      description="A global brand with local beginnings, our story begain in a small studio in South London in early 2014"
      colorTitle="#fff"
      colorDescription="#fff"
      background="var(--dark-primary)"
    />
    <img src="/img/room.jpg" alt="room" />
  </div>
</template>

<script setup>
import HeroInformation from "@/components/HeroInformation.vue";
</script>

<style lang="scss" scoped>
.ideas {
  padding: 0 80px;
  margin-bottom: 60px;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  column-gap: 16px;
}
</style>

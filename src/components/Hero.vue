<template>
  <div class="hero">
    <HeroInformation
      title="Luxury homeware for people who love timeless design quality"
      description="Shop the new Spring 2022 collection today"
      link="#"/>
  </div>
</template>

<script setup>
import HeroInformation from './HeroInformation.vue'
</script>

<style lang="scss" scoped>
.hero {
  background: url('https://amazingarchitecture.com/storage/1019/bedroom-minimalism.jpg');
  height: 704px;
  background-size: cover;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  padding-right: 80px;
  &-img {
    max-width: 100%;
  }
}
</style>
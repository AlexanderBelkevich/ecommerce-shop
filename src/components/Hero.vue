<template>
  <div class="hero">
    <HeroInformation
      title="Luxury homeware for people who love timeless design quality"
      description="Shop the new Spring 2022 collection today"
      link="#"
      colorLink="lightgray"
    />
    <img class="hero-image" src="/img/hero.jpg" alt="hero" />
  </div>
</template>

<script setup>
import HeroInformation from "@/components/HeroInformation.vue";
</script>

<style lang="scss" scoped>
.hero {
  background: url("/img/hero.jpg");
  height: 704px;
  background-size: cover;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  padding-right: 80px;
  @media screen and (max-width: 767px) {
    height: auto;
    background: transparent;
    padding-right: 0;
    display: block;
  }
  &-image {
    max-width: 100%;
    margin-top: 32px;
    display: none;
    @media screen and (max-width: 767px) {
      display: block;
    }
  }
}
</style>

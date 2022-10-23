<template>
  <div
    class="hero-info"
    :style="{ backgroundColor: background }"
    :class="{ 'hero-info--mobile-padding': mobilePadding }"
  >
    <div class="hero-info-text">
      <h2 class="hero-info__title" :style="{ color: colorTitle }">
        {{ title }}
      </h2>
      <span
        class="hero-info__description"
        :style="{ color: colorDescription }"
        >{{ description }}</span
      >
    </div>
    <ui-button
      :mobileFullWidth="true"
      :color="colorLink || 'secondary'"
      type="link"
      to="/"
    >
      View collection
    </ui-button>
  </div>
</template>

<script setup>
import uiButton from "@/components/UI/Button.vue";
const props = defineProps({
  title: {
    type: String,
    required: false,
  },
  description: {
    type: String,
    required: false,
  },
  link: {
    type: String,
    required: false,
  },
  colorTitle: {
    type: String,
    default: "",
  },
  colorDescription: {
    type: String,
    default: "#5B5676",
  },
  colorLink: {
    type: String,
    required: false,
  },
  background: {
    type: String,
    default: "#fff",
  },
  mobilePadding: {
    type: Boolean,
    default: false,
  },
});
</script>

<style lang="scss" scoped>
.hero {
  &-info {
    background: #fff;
    max-width: 630px;
    padding: 50px 55px;
    min-height: 444px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: flex-start;
    @media screen and (max-width: 767px) {
      padding: 47px 0 32px 0;
      min-height: 0;
    }
    &-text {
      @media screen and (max-width: 767px) {
        margin-bottom: 32px;
      }
    }
    &__title {
      font-family: var(--clash);
      font-weight: 400;
      line-height: 1.5;
      margin: 0 0 20px 0;
    }
    &__description {
      color: var(--lightGray);
      font-size: 18px;
    }
    &--mobile-padding {
      @media screen and (max-width: 767px) {
        padding: 36px 32px;
      }
    }
  }
}
</style>

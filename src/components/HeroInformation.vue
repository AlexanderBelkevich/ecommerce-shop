<template>
  <div class="hero-info" :style="{ backgroundColor: background }">
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
    <ui-button :color="colorLink || 'secondary'" type="link" to="/">
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
  }
}
</style>

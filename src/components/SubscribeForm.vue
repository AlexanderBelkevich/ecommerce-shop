<template>
  <form class="subscribe-form">
    <input
      type="text"
      placeholder="your@email.com"
      class="input-text subscribe-form__input"
      :style="{ background: bgInput, color: colorTextz }"
    />
    <ui-button :color="colorButton || 'dark-primary'">Sign Up</ui-button>
  </form>
</template>

<script setup>
import uiButton from "@/components/UI/Button.vue";

const props = defineProps({
  bgInput: {
    type: String,
    required: false,
  },
  colorButton: {
    type: String,
    required: false,
  },
  colorText: {
    type: String,
    required: false,
  },
});
</script>

<style lang="scss" scoped>
.subscribe-form {
  display: flex;
  &__input {
    flex-grow: 1;
  }
}
</style>

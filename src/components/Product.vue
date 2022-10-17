<template>
  <div class="product">
    <router-link to="/">
      <img :src="img" :alt="title" class="product-image" />
    </router-link>
    <router-link to="/" class="product-name">{{ title }}</router-link>
    <span class="product-price">£{{ price }}</span>
  </div>
</template>

<script setup>
const props = defineProps({
  img: {
    type: String,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
  price: {
    type: Number,
    required: true,
  },
});
</script>

<style lang="scss" scoped>
.product {
  &-image {
    display: block;
    margin-bottom: 24px;
  }
  &-name {
    display: block;
    color: var(--primary);
    font-size: 20px;
    line-height: 28px;
    font-family: var(--clash);
    margin-bottom: 8px;
    text-decoration: none;
    &:hover {
      text-decoration: underline;
    }
  }
  &-price {
    display: block;
    font-size: 18px;
    color: var(--primary);
  }
}
</style>

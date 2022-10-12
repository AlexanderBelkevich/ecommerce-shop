<template>
  <div class="product">
    <a href="#">
      <img :src="img" :alt="title" class="product-image">
    </a>
    <a href="#" class="product-name">{{title}}</a>
    <span class="product-price">£{{price}}</span>
  </div>
</template>

<script setup>
const props = defineProps({
  img: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  price: {
    type: Number,
    required: true
  }
})
</script>

<style lang="scss" scoped>
.product {
  &-image {
    display: block;
    margin-bottom: 24px;
  }
  &-name {
    display: block;
    color: #2A254B;
    font-size: 20px;
    line-height: 28px;
    font-family: 'Clash Display', sans-serif;
    margin-bottom: 8px;
    text-decoration: none;
    &:hover {
      text-decoration: underline;
    }
  }
  &-price {
    display: block;
    font-size: 18px;
    color: #2A254B;
  }
}
</style>
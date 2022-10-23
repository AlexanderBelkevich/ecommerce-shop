<template>
  <div>
    <Hero />
    <AboutBrand />
    <Loader v-if="loading" />
    <Products :products="popularProducts" v-else />
    <Ideas />
    <Subscribe />
  </div>
</template>

<script setup>
import { onMounted, ref } from "vue";
import api from "@/api";

import Loader from "@/components/UI/Loader.vue";
import Hero from "@/components/Hero.vue";
import AboutBrand from "@/components/AboutBrand.vue";
import Products from "@/components/Products4Column.vue";
import Ideas from "@/components/Ideas.vue";
import Subscribe from "@/components/Subscribe.vue";

const popularProducts = ref([]);
const loading = ref(true);

onMounted(async () => {
  popularProducts.value = await api.getPopularProducts();
  loading.value = false;
});
</script>

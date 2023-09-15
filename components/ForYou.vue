<template>
  <SectionHeader title="For You" class="mt-28" />
  <div class="grid grid-cols-5 gap-5 mx-32">
    <div v-for="p in products.products">
      <ProductCard :product="p" />
    </div>
  </div>
</template>

<script setup>
const { data: products } = await useFetch("https://dummyjson.com/products");
</script>

<style scoped></style>

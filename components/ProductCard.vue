<template>
  <div
    class="h-[335px] w-48 border-solid border border-slate-200 rounded-lg overflow-hidden font-poppins"
  >
    <img
      :src="product.thumbnail"
      alt="product"
      class="w-full h-44 object-cover"
    />

    <NuxtLink :to="`/products/${product.id}`">
      <button
        class="flex-start box-border h-40 w-48 p-4 border-0 bg-white hover:bg-gray-50 text-secondary"
      >
        <div
          class="box-border max-w-fit text-xs font-medium bg-gray-100 rounded-full py-1 px-2"
        >
          {{ product.category }}
        </div>
        <div class="mt-3 text-sm text-left line-clamp-2">
          {{ product.title }}
        </div>
        <div class="flex justify-between mt-2">
          <div class="font-semibold">Rp {{ product.price }}</div>
          <div class="mt-1 text-[11px] text-gray-400">450 ML</div>
        </div>
        <div class="flex justify-start">
          <div class="line-through text-[10px] text-gray-400 mt-1 mr-2">
            Rp 12
          </div>
          <div
            class="box-border w-auto text-center text-[10px] text-red-600 font-semibold bg-red-50 rounded-full py-1 px-2"
          >
            {{ product.discountPercentage }} %
          </div>
        </div>
      </button>
    </NuxtLink>
  </div>
</template>

<script setup>
const { product } = defineProps(["product"]);
</script>

<style scoped>
.thumb {
  max-height: 120px;
  max-width: 70%;
  margin: 0 auto;
}
</style>

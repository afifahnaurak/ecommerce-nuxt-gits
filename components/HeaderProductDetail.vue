<template>
  <div class="bg-gradient-to-b from-primary from-30% h-36">
    <div class="flex justify-between pt-10 mx-32">
      <button
        class="bg-white border border-slate-200 hover:bg-slate-400 rounded-md px-3"
      >
        <NuxtLink to="/products">
          <div class="flex justify-center gap-1">
            <div>
              <img src="~/assets/icons/arrow-left.svg" width="20" />
            </div>
            <div class="font-poppins font-medium text-sm text-secondary">
              Back
            </div>
          </div>
        </NuxtLink>
      </button>
      <div class="text-3xl font-poppins font-semibold text-secondary pl-10">
        Product Detail
      </div>
      <button
        class="bg-sky-600 border border-slate-200 hover:bg-sky-700 rounded-md px-3"
        @click="cart.addItem(product.id)"
      >
        <div class="flex justify-center gap-1">
          <div>
            <img src="~/assets/icons/plus.svg" width="20" />
          </div>
          <div class="font-poppins font-medium text-sm text-white">
            Add to Cart
          </div>
        </div>
      </button>
    </div>
  </div>
</template>

<script setup>
import { useCart } from "~/store/cart";
const cart = useCart();
</script>

<style scoped></style>

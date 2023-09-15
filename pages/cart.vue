<template>
  <div>
    <Header title="Shopping Cart" class="flex justify-start" />
    <div class="flex justify-between gap-2 mx-32 mb-16 mt-12">
      <div class="grid grid-cols-1 gap-5">
        <div v-for="p in cart.cart.products">
          <ProductCart :product="p" />
        </div>
      </div>
      <CartTotal :total="cart.cart.total" />
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "pages",
});
import { useCart } from "~/store/cart";
const cart = useCart();
</script>

<style scoped></style>

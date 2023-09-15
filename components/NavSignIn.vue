<template>
  <div>
    <header
      class="flex justify-between items-center bg-primary w-min-full px-32 py-2"
    >
      <nav class="container mx-auto flex justify-between">
        <div class="flex justify-between">
          <NuxtLink to="/">
            <div class="flex flex-start gap-x-2 py-4">
              <img src="~/assets/icons/Content.svg" width="30" />
              <img src="~/assets/icons/Gits1.svg" width="110" />
            </div>
          </NuxtLink>
          <ul
            class="font-poppins flex justify-evenly text-base font-medium gap-x-6 py-4 text-gray-600 mt-2"
          >
            <li><NuxtLink to="/">Home</NuxtLink></li>
            <li><NuxtLink to="/products">Products</NuxtLink></li>
            <li><NuxtLink to="/categories">Categories</NuxtLink></li>
          </ul>
        </div>
        <div>
          <ul
            class="font-poppins flex justify-evenly text-base font-medium gap-x-6 py-4 text-gray-600 mt-2"
          >
            <li>
              <NuxtLink
                to="/cart"
                class="relative w-10 h-10 flex items-center justify-center"
              >
                <span
                  class="absolute top-1 right-0 w-4 h-4 rounded-full bg-orange-500 text-[10px] text-white text-center flex justify-center items-center"
                  >{{ cart.cart ? cart.cart.totalProducts : 0 }}</span
                >
                <img src="~/assets/icons/shopping-cart.svg" alt="cart" />
              </NuxtLink>
            </li>
            <li>
              <NuxtLink to="/profile">
                <img src="~/assets/images/avatar.png" width="35" />
              </NuxtLink>
            </li>
          </ul>
        </div>
      </nav>
    </header>
  </div>
</template>

<script setup>
import { useCart } from "~/store/cart";
const cart = useCart();

onMounted(() => {
  cart.fetchCart();
});
</script>

<style scoped>
.router-link-exact-active {
  font-weight: bold;
  color: rgb(55 65 81);
}
</style>

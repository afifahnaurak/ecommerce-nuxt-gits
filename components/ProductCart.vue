<template>
  <div
    class="flex h-[150px] w-[580px] border-solid border border-slate-200 rounded-lg overflow-hidden"
  >
    <img
      :src="`https://i.dummyjson.com/data/products/${product.id}/thumbnail.jpg`"
      alt="product"
      class="h-[140px] w-[240px] rounded-md overflow-hidden object-cover ml-1 mt-1 flex items-center justify-center"
    />
    <div :to="`/products/${product.id}`">
      <button
        class="box-border h-44 w-[330px] p-4 border-0 bg-white text-secondary"
      >
        <div class="grid grid-row-2 gap-14 -mt-7">
          <div>
            <div class="flex justify-between">
              <div class="text-sm text-left font-medium line-clamp-2 w-[220px]">
                {{ product.title }}
              </div>
              <div class="font-bold">Rp {{ product.price }}</div>
            </div>
            <div class="flex justify-start text-[10px] text-gray-400 mt-1">
              Color Name
            </div>
          </div>
          <div class="flex justify-between">
            <div class="text-base text-left w-[220px]">Qty: 1</div>
            <button>
              <div
                class="flex jusify-center gap-1"
                @click="cart.removeItem(product.id)"
              >
                <div>
                  <img src="~/assets/icons/trash.svg" width="15" />
                </div>
                <div class="font-poppins font-semibold text-xs text-red-800">
                  Remove
                </div>
              </div>
            </button>
          </div>
        </div>
      </button>
    </div>
  </div>
</template>

<script setup>
import { useCart } from "~/store/cart";
const cart = useCart();

const { product } = defineProps(["product"]);
</script>

<style scoped>
.thumb {
  max-height: 120px;
  max-width: 70%;
  margin: 0 auto;
}
</style>

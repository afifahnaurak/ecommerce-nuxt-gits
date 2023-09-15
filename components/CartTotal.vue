<template>
  <div
    class="flex h-[160px] w-[410px] border-solid border border-slate-200 rounded-lg overflow-hidden"
  >
    <div
      class="box-border h-48 w-[410px] p-4 border-0 bg-white text-secondary font-poppins"
    >
      <div class="flex justify-between">
        <div class="text-sm font-medium text-left w-[100px]">Sub Total</div>
        <div class="font-bold">Rp {{ total }}</div>
      </div>
      <div class="text-sm text-gray-400 mt-1">
        <div>Shipping and taxes</div>
        <div>calculated at checkout</div>
      </div>
      <button
        class="bg-blue-500 hover:bg-sky-700 text-white p-2 w-full rounded-md mt-4"
      >
        <NuxtLink to="/success">
          <div class="flex justify-center items-center gap-2">
            <div>
              <img src="~/assets/icons/arrow-right-white.svg" />
            </div>
            <div>Checkout</div>
          </div>
        </NuxtLink>
      </button>
    </div>
  </div>
</template>

<script setup>
defineProps({
  total: Number,
});
</script>

<style scoped>
.thumb {
  max-height: 120px;
  max-width: 70%;
  margin: 0 auto;
}
</style>

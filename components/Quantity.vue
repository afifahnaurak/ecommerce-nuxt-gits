<template>
  <div class="flex justify-start gap-2">
    <button
      class="bg-gray-200 rounded-md text-white text-2xl text-center h-10 w-10 pb-1"
      @click="discrement"
    >
      -
    </button>
    <input
      :value="qty"
      class="font-poppins text-center w-10 border border-gray-300 rounded-md text-md bg-white text-black"
      @keydown.enter.prevent=""
    />
    <button
      class="bg-sky-600 rounded-md text-white text-2xl text-center h-10 w-10 pb-1"
      @click="increment"
    >
      +
    </button>
  </div>
</template>

<script setup lang="ts">
const qty = ref(1);

const increment = (): void => {
  qty.value++;
};

const discrement = (): void => {
  if (qty.value > 1) {
    qty.value--;
  }
};

defineProps({
  modelValue: Number,
});
</script>

<style scoped></style>

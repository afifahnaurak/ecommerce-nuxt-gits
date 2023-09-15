<template>
  <div class="flex justify-start gap-2">
    <button
      :disabled="!available"
      :class="`${
        status && available
          ? variants.active
          : available
          ? variants.available
          : variants.nonAvailable
      } flex justify-center items-center gap-1 w-36 px-1 py-1 rounded-md`"
      :style="{ cursor: available ? 'pointer' : 'not-allowed' }"
    >
      <span
        :class="`rounded-full ${color ? colors[color] : ''} h-8 w-8`"
      ></span>
      <span class="">Color Name</span>
    </button>
  </div>
</template>

<script setup lang="ts">
defineProps({
  color: String,
  available: Boolean,
  status: Boolean,
});

const colors: { [key: string]: string } = {
  orange: "bg-orange-600",
  green: "bg-green-600",
  blue: "bg-blue-600",
};

const variants: { [key: string]: string } = {
  active: "border-2 border-sky-500 rounded-md text-secondary",
  available: "bg-gray-100 rounded-md text-secondary",
  nonAvailable: "bg-gray-200 rounded-md text-white",
};
</script>

<style scoped></style>

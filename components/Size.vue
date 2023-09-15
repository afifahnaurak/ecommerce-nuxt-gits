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
      } flex justify-center items-center gap-2 w-12 pt-1 rounded-md`"
      :style="{ cursor: available ? 'pointer' : 'not-allowed' }"
    >
      <span class="h-8 w-8">{{ size }}</span>
    </button>
  </div>
</template>

<script setup lang="ts">
defineProps({
  size: String,
  available: Boolean,
  status: Boolean,
});

const variants: { [key: string]: string } = {
  active: "border-2 border-sky-500 rounded-md text-secondary",
  available: "bg-gray-100 rounded-md text-secondary",
  nonAvailable: "bg-gray-200 rounded-md text-white",
};
</script>

<style scoped></style>

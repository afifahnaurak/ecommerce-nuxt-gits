<template>
  <div>
    <div
      :class="`w-10 h-10 rounded-lg ${
        active ? 'bg-gray-200' : ''
      } flex items-center justify-center text-sm font-medium text-gray-800`"
    >
      {{ number }}
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps({
  active: Boolean,
  number: Number,
});
</script>

<style scoped></style>

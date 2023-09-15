<template>
  <div class="bg-gradient-to-b from-primary from-30% h-40 pt-6 -mb-16">
    <div class="pt-10 mx-32">
      <div class="text-3xl font-poppins font-semibold text-secondary">
        {{ title }}
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps({
  title: String,
});
</script>

<style scoped></style>

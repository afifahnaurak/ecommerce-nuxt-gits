<template>
  <div class="flex justify-between my-6 mx-32 md:mx-32">
    <div class="font-poppins font-bold text-secondary text-lg">{{ title }}</div>
    <div
      class="flex justify-evenly gap-2 text-sky-600 font-poppins font-bold text-sm"
    >
      <NuxtLink to="/" class="flex">
        <div class="mr-1">View All</div>
        <img src="~/assets/icons/Arrow-Right.svg" width="20" class="-mt-2" />
      </NuxtLink>
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: String,
});
</script>

<style scoped></style>

<template>
  <div>
    <SectionHeader title="Categories" />
    <div class="px-32 pb-20 flex justify-between flex-wrap">
      <button
        class="place-items-center text-center"
        v-for="item in categories"
        :key="item.title"
      >
        <img
          :src="`/assets/icons/cat/${item.fileName}.svg`"
          width="90"
          class="mx-7 text-center"
        />
        <div class="mt-4 font-poppins font-medium w-[150px]">
          {{ item.title }}
        </div>
      </button>
    </div>
  </div>
</template>

<script setup>
import categories from "~/server/api/category.json";
</script>

<style scoped></style>

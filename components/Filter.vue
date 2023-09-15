<template>
  <div>
    <div class="font-poppins font-semibold mb-4 mr-20">Heading</div>
    <div class="font-poppins text-sm" v-for="item in filters" :key="item.title">
      <div class="flex justify-start gap-2 mt-3">
        <input type="checkbox" class="form-checkbox h-4 w-4 mt-[2px]" />
        <div>
          {{ item.title }}
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import filters from "~/server/api/filter.json";
</script>

<style scoped></style>

<template>
  <button
    class="bg-white border border-slate-200 hover:bg-slate-400 rounded-md px-3"
  >
    <NuxtLink to="/products">
      <div class="flex justify-center gap-1">
        <div>
          <img src="~/assets/icons/arrow-left.svg" width="20" />
        </div>
        <div class="font-poppins font-medium text-sm text-secondary">Back</div>
      </div>
    </NuxtLink>
  </button>
</template>

<script setup lang="ts"></script>

<style scoped></style>

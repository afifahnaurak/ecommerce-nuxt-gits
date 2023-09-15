<template>
  <div class="bg-gradient-to-b from-primary from-30% h-40">
    <div class="flex justify-center mx-32 pt-24">
      <div class="text-2xl font-poppins font-semibold text-secondary">
        Thank you!
      </div>
    </div>
    <div class="flex justify-center">
      <div class="font-poppins font-normal text-lg text-gray-400 mt-2">
        Your order will be processed immediately.
      </div>
    </div>
    <div class="flex justify-center pt-10 mx-32">
      <button
        class="bg-sky-600 border border-slate-200 hover:bg-sky-700 rounded-md px-3 py-3"
      >
        <NuxtLink to="/">
          <div class="flex justify-center gap-1">
            <div>
              <img src="~/assets/icons/home.svg" width="20" />
            </div>
            <div class="font-poppins font-medium text-sm text-white">
              Back to Home
            </div>
          </div>
        </NuxtLink>
      </button>
    </div>
  </div>
  <div class="bg-white h-72"></div>
</template>

<script setup></script>

<style scoped></style>

<template>
  <div>
    <header
      class="flex justify-between items-center bg-primary w-min-full px-32 py-2"
    >
      <nav class="container mx-auto flex justify-between">
        <div class="flex justify-between">
          <NuxtLink to="/">
            <div class="flex flex-start gap-x-2 py-4">
              <img src="~/assets/icons/Content.svg" width="30" />
              <img src="~/assets/icons/Gits1.svg" width="110" />
            </div>
          </NuxtLink>
          <ul
            class="font-poppins flex justify-evenly text-base font-medium gap-x-6 py-4 text-gray-600 mt-2"
          >
            <li><NuxtLink to="/">Home</NuxtLink></li>
            <li><NuxtLink to="/products">Products</NuxtLink></li>
            <li><NuxtLink to="/categories">Categories</NuxtLink></li>
          </ul>
        </div>
        <div>
          <ul
            class="font-poppins flex justify-evenly text-base font-medium gap-x-6 py-4 text-gray-600 mt-2"
          >
            <li><NuxtLink to="/login">Log in</NuxtLink></li>
            <li
              class="bg-sky-600 hover:bg-sky-700 text-white p-2 -my-2 rounded-md"
            >
              <NuxtLink to="/signup">Sign up</NuxtLink>
            </li>
          </ul>
        </div>
      </nav>
    </header>
  </div>
</template>

<script setup></script>

<style scoped>
.router-link-exact-active {
  font-weight: bold;
  color: rgb(55 65 81);
}
</style>

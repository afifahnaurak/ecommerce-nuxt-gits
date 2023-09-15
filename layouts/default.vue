<template>
  <div>
    <Nav />

    <div class="container mx-auto">
      <slot />
    </div>

    <Footer />
  </div>
</template>

<script setup></script>

<style scoped>
.router-link-exact-active {
  font-weight: bold;
  color: rgb(55 65 81);
}
</style>

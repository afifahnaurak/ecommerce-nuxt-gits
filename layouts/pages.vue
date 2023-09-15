<template>
  <div>
    <NavSignIn />

    <div class="container mx-auto">
      <slot />
    </div>

    <FooterPage />
  </div>
</template>

<script setup></script>

<style scoped>
.router-link-exact-active {
  font-weight: bold;
  color: rgb(55 65 81);
}
</style>

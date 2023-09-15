<template>
  <div>
    <Header title="Product List" class="flex justify-center" />
    <div class="flex justify-center">
      <form @submit.prevent="" class="mt-6 mb-6 mr-3">
        <div class="relative flex items-center">
          <span
            class="w-5 h-5 absolute ml-4 mb-1 icon-pencil pointer-events-none"
          >
            <img src="~/assets/icons/search.svg" width="30" />
          </span>
          <input
            v-model="query"
            placeholder="Search"
            class="font-poppins pl-10 pr-72 py-2 border rounded-md text-md bg-white text-black"
            @keydown.enter.prevent="search(query)"
          />
        </div>
      </form>
      <button
        class="bg-white border border-slate-200 hover:bg-slate-400 rounded-md px-3 mt-6 mb-6"
      >
        <div class="flex justify-center gap-1">
          <div>
            <img src="~/assets/icons/Sort.svg" width="20" />
          </div>
          <div class="font-poppins font-medium text-sm text-secondary">
            Sort by
          </div>
        </div>
      </button>
    </div>
    <div class="flex justify-start gap-5 ml-32 mt-8">
      <div>
        <Filter />
        <Filter class="mt-10" />
      </div>
      <div>
        <div class="grid grid-cols-4 gap-5 mr-32 pl-6 border-l-[1.5px]">
          <div v-for="p in data">
            <ProductCard :product="p" />
          </div>
        </div>
        <Pagination />
      </div>
    </div>
  </div>
</template>

<script setup>
import axios from "axios";

async function fecthData() {
  const response = await axios.get("https://dummyjson.com/products/");
  data.value = response.data.products;
}

definePageMeta({
  layout: "pages",
});

onMounted(() => {
  fecthData();
});

async function search(query) {
  const response = await axios.get(
    `https://dummyjson.com/products/search?q=${query}`
  );
  data.value = response.data.products;
}

const query = ref("");

const data = ref([]);
</script>

<style scoped></style>

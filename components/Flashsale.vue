<template>
  <div class="bg-slate-50 py-12 font-poppins">
    <div class="flex justify-between mb-6 mx-auto px-32">
      <div class="flex justify-evenly gap-2">
        <div class="font-bold text-secondary text-lg">Flash Sale</div>
        <div class="font-medium text-white bg-red-500 rounded-md py-1 px-2">
          00 : 12 : 12
        </div>
      </div>
      <div
        class="flex justify-evenly gap-2 text-sky-600 font-poppins font-bold text-sm"
      >
        <button class="flex">
          <div class="mr-1">View All</div>
          <img src="~/assets/icons/Arrow-Right.svg" width="20" />
        </button>
      </div>
    </div>
    <div class="px-24">
      <Swiper
        :modules="modules"
        :slides-per-view="5"
        :space-between="25"
        :loop="true"
        :navigation="{ enabled: true, nextEl: '.swiper-button-next' }"
        :autoplay="{
          delay: 7000,
          disableOnInteraction: false,
          pauseOnMouseEnter: true,
        }"
      >
        <SwiperSlide v-for="p in products.products">
          <ProductCard :product="p" />
        </SwiperSlide>
        <div
          class="swiper-button-next w-8 h-8 bg-gray-400 absolute z-10 right-0 top-[155px] rounded-full mr-[1px] mb-12"
        >
          <img src="~/assets/icons/Right.svg" />
        </div>
      </Swiper>
    </div>
  </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, Autoplay } from "swiper/modules";
import "swiper/css";

const modules = [Navigation, Autoplay];

const { data: products } = await useFetch("https://dummyjson.com/products");
</script>

<style scoped>
.swiper {
  padding: 0 18px;
  overflow: hidden;
}
</style>

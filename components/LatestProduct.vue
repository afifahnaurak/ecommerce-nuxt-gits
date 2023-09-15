<template>
  <div>
    <SectionHeader title="Latest Product" class="mt-16" />
    <div class="px-24 ml-8">
      <div
        class="flex-start box-border h-auto w-[263px] p-4 border-0 bg-sky-500 rounded-2xl text-secondary font-poppins"
      >
        <div class="self-stretch text-2xl text-white mt-4">Discount</div>
        <div class="self-stretch text-5xl font-bold text-white leading-[60px]">
          More and More
        </div>
        <div class="text-2xl text-white mt-12">Up To</div>
        <div class="text-5xl font-bold text-yellow-300 mt-2 mb-4">50%</div>
      </div>
      <div class="pl-48 mt-[-380px]">
        <Swiper
          :modules="modules"
          :slides-per-view="4"
          :space-between="5"
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
  </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, Autoplay } from "swiper/modules";
import "swiper/css";

const modules = [Navigation, Autoplay];

const { data: products } = await useFetch("https://dummyjson.com/products");
</script>

<style scoped></style>

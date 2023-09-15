<template>
  <div class="bg-gradient-to-b from-primary from-30% h-36">
    <div class="flex justify-between pt-10 mx-32">
      <button
        class="bg-white border border-slate-200 hover:bg-slate-400 rounded-md px-3"
      >
        <NuxtLink to="/products">
          <div class="flex justify-center gap-1">
            <div>
              <img src="~/assets/icons/arrow-left.svg" width="20" />
            </div>
            <div class="font-poppins font-medium text-sm text-secondary">
              Back
            </div>
          </div>
        </NuxtLink>
      </button>
      <div class="text-3xl font-poppins font-semibold text-secondary pl-10">
        Product Detail
      </div>
      <button
        class="bg-sky-600 border border-slate-200 hover:bg-sky-700 rounded-md px-3"
        @click="cart.addItem(product.id, Number(qty))"
      >
        <div class="flex justify-center gap-1">
          <div>
            <img src="~/assets/icons/plus.svg" width="20" />
          </div>
          <div class="font-poppins font-medium text-sm text-white">
            Add to Cart
          </div>
        </div>
      </button>
    </div>
  </div>
  <div class="h-full ml-32">
    <div class="grid grid-cols-2">
      <div class="pe-8">
        <Swiper
          class="overflow-hidden"
          :modules="modules"
          :slides-per-view="1"
          :loop="false"
          :thumbs="{ multipleActiveThumbs: false, swiper: thumbsSwiper }"
        >
          <SwiperSlide v-for="image in product.images">
            <img
              :src="image"
              alt="product img"
              class="max-h-[450px] max-w-full min-h-[450px] min-w-full object-cover rounded-xl"
            />
          </SwiperSlide>
        </Swiper>

        <div class="mt-3 max-w-full">
          <Swiper
            class="overflow-hidden"
            :modules="modules"
            @swiper="setThumbSwiper"
            :slides-per-view="4"
            :space-between="10"
            :loop="false"
            :navigation="{ enabled: true, nextEl: '.swiper-button-next' }"
            :autoplay="{
              delay: 7000,
              disableOnInteraction: false,
              pauseOnMouseEnter: true,
            }"
          >
            <SwiperSlide v-for="image in product.images">
              <img
                :src="image"
                alt="product img"
                class="h-[105px] w-full object-cover rounded-xl"
              />
            </SwiperSlide>
          </Swiper>
        </div>
      </div>
      <div class="mr-32">
        <h2 class="text-2xl font-bold">
          {{ product.title }}
        </h2>
        <p class="text-xl font-bold text-sky-700">Rp {{ product.price }}</p>
        <h3 class="font-medium text-slate-500 mb-1 mt-6">Color</h3>
        <div class="flex justify-start gap-2">
          <Color
            v-for="color in colors"
            :available="color.available"
            :status="color.status"
            :color="color.color"
            @click="colorHandler(color)"
          />
        </div>
        <h3 class="font-medium text-slate-500 mb-1 mt-6">Size</h3>
        <div class="flex justify-start gap-2">
          <Size
            v-for="size in sizes"
            :available="size.available"
            :status="size.status"
            :size="size.size"
            @click="sizeHandler(size)"
          />
        </div>
        <h3 class="font-medium text-slate-500 mb-1 mt-6">Quantity</h3>
        <div class="flex justify-start gap-2">
          <button
            class="bg-gray-200 rounded-md text-white text-2xl text-center h-10 w-10 pb-1"
            @click="discrement"
          >
            -
          </button>
          <input
            :value="qty"
            class="font-poppins text-center w-10 border border-gray-300 rounded-md text-md bg-white text-black"
            @keydown.enter.prevent=""
          />
          <button
            class="bg-sky-600 rounded-md text-white text-2xl text-center h-10 w-10 pb-1"
            @click="increment"
          >
            +
          </button>
        </div>
        <div class="flex justify-between items-center mb-1 mt-6">
          <h3 class="font-medium text-slate-500">Description</h3>
          <button
            class="border border-blue-200 rounded-md w-6 h-6 pb-1 text-center flex justify-center items-center text-blue-500 text-2xl"
          >
            -
          </button>
        </div>
        <p class="font-semibold text-violet-950 mb-7">
          {{ product.description }}
        </p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, Autoplay, Thumbs, FreeMode } from "swiper/modules";
import "swiper/css";

import { useCart } from "~/store/cart";
const cart = useCart();

const qty = ref(1);
const increment = (): void => {
  qty.value++;
};

const discrement = (): void => {
  if (qty.value > 1) {
    qty.value--;
  }
};

const modules = [Navigation, Autoplay, Thumbs, FreeMode];

const { product } = defineProps(["product"]);

const thumbsSwiper = ref(null);

const setThumbSwiper = (swiper: any) => {
  thumbsSwiper.value = swiper;
};

const colorHandler = (color: any) => {
  colors.value.map((item) => {
    item.status = false;
  });
  color.status = true;
};

const sizeHandler = (size: any) => {
  sizes.value.map((item) => {
    item.status = false;
  });
  size.status = true;
};

const colors = ref([
  {
    color: "orange",
    available: true,
    status: true,
  },
  {
    color: "green",
    available: true,
    status: false,
  },
  {
    color: "blue",
    available: false,
    status: false,
  },
]);

const sizes = ref([
  {
    size: "S",
    available: true,
    status: false,
  },
  {
    size: "M",
    available: false,
    status: false,
  },
  {
    size: "L",
    available: true,
    status: false,
  },
  {
    size: "XL",
    available: true,
    status: true,
  },
]);
</script>

<style scoped>
img {
  max-width: 400px;
}

.swiper {
  padding: 0 0px;
  overflow: hidden;
}

.swiper-slide-thumb-active {
  border: 2px solid #0984dd;
  border-radius: 16px;
  overflow: hidden;
}
</style>

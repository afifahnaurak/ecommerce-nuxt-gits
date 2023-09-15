<template>
  <div class="flex justify-between mt-6 border-t-[1.5px] pt-6 mr-32">
    <button
      class="flex justify-center gap-1 border-[1.5px] px-3 py-2 rounded-md hover:bg-slate-100"
    >
      <div>
        <img src="~/assets/icons/arrow-left.svg" width="20" />
      </div>
      <div class="font-poppins font-medium text-sm text-secondary">
        Previous
      </div>
    </button>
    <button>
      <ul class="flex">
        <PaginationNumber :active="true" :number="1" />
        <PaginationNumber :active="false" :number="2" />
        <PaginationNumber :active="false" :number="3" />
        <PaginationNumber :active="false" :number="4" />
        <PaginationNumber :active="false" :number="5" />
        <PaginationNumber :active="false" :number="6" />
      </ul>
    </button>

    <button
      class="flex justify-center gap-1 border-[1.5px] px-3 py-2 rounded-md hover:bg-slate-100"
    >
      <div class="font-poppins font-medium text-sm text-secondary">Next</div>
      <div>
        <img src="~/assets/icons/arrow-right-black.svg" width="20" />
      </div>
    </button>
  </div>
</template>

<script setup></script>

<style scoped></style>

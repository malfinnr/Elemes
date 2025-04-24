<template>
  <div
    class="bg-white/74 shadow-[0px_11px_39px_rgba(0,0,0,0.07)] rounded-[17px] backdrop-blur-[5.5px] lg:w-[292px] h-[93px] flex items-center gap-5 py-3 px-6"
  >
    <img
      src="@/assets/hero/salad.webp"
      class="w-13 h-13 rounded-full object-cover"
      alt=""
    />
    <div class="flex flex-col gap-y-2.25">
      <div>
        <h3 class="text-sm/6 font-semibold text-black">Green Salad Tomato</h3>
        <p class="text-dark/40 font-normal text-xs">Tomato</p>
      </div>
      <StarRating :filled="4" />
    </div>
  </div>
</template>

<script setup lang="ts">
import StarRating from "./StarRating.vue";
</script>

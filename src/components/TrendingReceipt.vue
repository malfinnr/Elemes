<template>
  <div class="relative lg:px-10 px-4 mt-20 lg:my-[114px]">
    <div class="mb-8">
      <h2 class="font-medium text-2xl/[30px] lg:text-[38px]/[50px]">
        Browser Our Trending <br />
        <span class="text-primary">Receipt</span>
      </h2>
    </div>
    <div
      class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-x-5 gap-y-5 sm:gap-y-7.5"
    >
      <div v-for="card in cards" :key="card.id">
        <div
          class="relative w-full h-full rounded-[17px] py-7.5 px-6 shrink-0 flex flex-col text-dark text-left"
          :style="{ backgroundColor: card.backgroundColor }"
        >
          <img
            src="@/assets/receipt/background.webp"
            alt=""
            class="absolute inset-0 object-cover opacity-0 hover:opacity-100 transition-opacity duration-300 z-0"
          />
          <img
            :src="card.image"
            alt="Card Image"
            class="size-[120px] object-cover rounded-md"
          />
          <div class="my-5">
            <h6 class="text-2xl font-medium">{{ card.title }}</h6>
            <p class="text-lg font-medium text-primary mt-1">
              {{ card.category }}
            </p>
          </div>
          <div>
            <StarRating :filled="card.star" />
          </div>
        </div>
      </div>
    </div>
    <div class="flex justify-center mt-[68px]">
      <button
        class="bg-primary py-4 px-5 text-base font-medium text-white rounded-full"
      >
        All Receipt
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">
import cupcakechoco from "@/assets/trending/cupcakechoco.png";
import donerkebab from "@/assets/trending/donerkebab.png";
import doughnut from "@/assets/trending/doughnut.png";
import doughnutunicorn from "@/assets/trending/doughnutunicorn.png";
import kebabrathi from "@/assets/trending/kebabssss.png";
import pizzameat from "@/assets/trending/pizzameat.png";
import pizzapeperoni from "@/assets/trending/pizzapeperoni.png";
import salmonroll from "@/assets/trending/salmonroll.png";
import StarRating from "./StarRating.vue";

const cards = [
  {
    id: 1,
    title: "Pizza Paperoni",
    category: "Pizza",
    image: pizzapeperoni,
    star: 4,
    backgroundColor: "#e6f3f5",
  },
  {
    id: 2,
    title: "Pizza Meat",
    category: "Pizza",
    image: pizzameat,
    star: 3,
    backgroundColor: "#e6f3f5",
  },
  {
    id: 3,
    title: "Doner Kebab",
    category: "Kebab",
    image: donerkebab,
    star: 5,
    backgroundColor: "#EAEEFA",
  },
  {
    id: 4,
    title: "Salmon Roll",
    category: "Salmon",
    image: salmonroll,
    star: 4,
    backgroundColor: "#f9eef3",
  },
  {
    id: 5,
    title: "Cupcake Choco",
    category: "Cupcake",
    image: cupcakechoco,
    star: 4,
    backgroundColor: "#f0feeb",
  },
  {
    id: 6,
    title: "Dougnhnut Milk",
    category: "Doughnut",
    image: doughnut,
    star: 5,
    backgroundColor: "#f3f7d9",
  },
  {
    id: 7,
    title: "Doughnut Unicorn",
    category: "Doughnut",
    image: doughnutunicorn,
    star: 4,
    backgroundColor: "#f3f7d9",
  },
  {
    id: 8,
    title: "Kathi Kebab",
    category: "Kebab",
    image: kebabrathi,
    star: 4,
    backgroundColor: "#eaeefa",
  },
];
</script>

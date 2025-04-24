<template>
  <div class="relative lg:pl-10">
    <div class="mb-8 max-lg:pl-4">
      <h2 class="font-medium text-2xl/[30px] lg:text-[38px]/[50px]">
        Browser Our Category <br />
        <span class="text-primary">Receipt</span>
      </h2>
    </div>
    <div
      ref="scrollContainer"
      class="flex overflow-x-auto overflow-y-hidden pb-10 lg:snap-x lg:snap-start scroll-smooth gap-2.5 max-lg:first:pl-4 max-lg:pr-4"
    >
      <div v-for="card in cards" :key="card.id">
        <div
          class="relative min-w-[230px] h-[175px] transform transition-transform origin-top duration-300 hover:scale-y-110 rounded-lg p-7.5 snap-start shrink-0 flex flex-col items-center justify-between text-dark text-center"
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
            class="w-11.75 h-11.75 object-contain"
          />
          <div>
            <h6 class="text-base font-medium">{{ card.title }}</h6>
            <p class="text-sm mt-1">{{ card.total_items }} items</p>
          </div>
        </div>
      </div>
    </div>

    <div
      class="hidden lg:flex justify-end items-center gap-3 mt-2.5 pr-4 lg:pr-10"
    >
      <button
        @click="scrollPrev"
        class="px-3.25 py-2 h-12.5 w-[113px] bg-primary text-white text-base font-medium uppercase rounded-full hover:bg-primary/70 inline-flex items-center gap-1.75"
      >
        <span
          class="rounded-full bg-white size-8.25 flex items-center justify-center"
        >
          <IconArrowLeft />
        </span>
        Prev
      </button>
      <button
        @click="scrollNext"
        class="px-3.25 py-2 h-12.5 w-[113px] bg-primary text-white text-base font-medium uppercase rounded-full hover:bg-primary/70 inline-flex items-center gap-1.75"
      >
        Next
        <span
          class="rounded-full bg-white size-8.25 flex items-center justify-center rotate-180"
        >
          <IconArrowLeft />
        </span>
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import cupcake from "@/assets/receipt/cupcake.webp";
import pizza from "@/assets/receipt/pizza.webp";
import salmon from "@/assets/receipt/salmon.webp";
import doughnut from "@/assets/receipt/doughnut.webp";
import kebab from "@/assets/receipt/kebab.webp";
import IconArrowLeft from "./icons/IconArrowLeft.vue";

const scrollContainer = ref(null);

const cards = [
  {
    id: 1,
    title: "Cupcake",
    total_items: 22,
    image: cupcake,
    backgroundColor: "#f0feeb",
  },
  {
    id: 2,
    title: "Pizza",
    total_items: 25,
    image: pizza,
    backgroundColor: "#e4f2f4",
  },
  {
    id: 3,
    title: "Kebab",
    total_items: 12,
    image: kebab,
    backgroundColor: "#EAEEFA",
  },
  {
    id: 4,
    title: "Salmon",
    total_items: 22,
    image: salmon,
    backgroundColor: "#f9eef3",
  },
  {
    id: 5,
    title: "Doughnut",
    total_items: 11,
    image: doughnut,
    backgroundColor: "#f3f7d9",
  },
];

const scrollAmount = 240;

const scrollNext = () => {
  (scrollContainer?.value as any)?.scrollBy({
    left: scrollAmount,
    behavior: "smooth",
  });
};

const scrollPrev = () => {
  (scrollContainer?.value as any)?.scrollBy({
    left: -scrollAmount,
    behavior: "smooth",
  });
};
</script>

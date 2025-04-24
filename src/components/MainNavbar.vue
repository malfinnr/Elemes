<template>
  <div class="bg-white">
    <header class="absolute inset-x-0 top-0 z-50">
      <nav
        class="flex items-center justify-between p-6 lg:px-8"
        aria-label="Global"
      >
        <div class="flex lg:flex-1">
          <a href="#" class="-m-1.5 p-1.5">
            <span class="sr-only">Your Company</span>
            <img class="lg:h-12.5 h-9 w-auto" src="@/assets/logo.webp" alt="" />
          </a>
        </div>
        <div class="hidden lg:flex lg:gap-x-8">
          <RouterLink
            v-for="item in navigation"
            :key="item.name"
            :to="item.href"
            class="text-sm font-medium text-light-1"
            >{{ item.name }}</RouterLink
          >
        </div>
        <div class="flex flex-1 justify-end">
          <div class="flex items-center gap-6">
            <a href="#" class="max-lg:hidden text-sm font-medium text-dark"
              >Masuk</a
            >
            <button
              class="bg-primary cursor-pointer rounded-full text-white text-sm font-medium py-2.5 px-4.5"
            >
              Daftar Sekarang
            </button>
          </div>
        </div>
      </nav>
    </header>
  </div>
</template>
<script setup lang="ts">
import { RouterLink } from "vue-router";

const navigation = [
  { name: "Home", href: "/" },
  { name: "About", href: "#" },
  { name: "Promotions", href: "#" },
  { name: "Blogs", href: "#" },
  { name: "Contact Us", href: "#" },
];
</script>

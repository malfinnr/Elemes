<template>
  <div class="relative isolate lg:pt-8 max-lg:pb-[128px] pt-[89px]">
    <div class="absolute inset-0 -z-10 size-full" aria-hidden="true">
      <img
        src="@/assets/hero/background.webp"
        alt=""
        class="size-full object-cover opacity-2"
      />
    </div>
    <div class="px-4 lg:px-10 lg:flex lg:items-center lg:gap-x-10">
      <div class="mx-auto max-w-2xl lg:mx-0 lg:flex-auto">
        <h1 class="mt-10 text-5xl font-medium text-primary sm:text-[64px]">
          Good Food Us <br />
          Good Mood
        </h1>
        <p class="mt-8 text-lg font-normal text-light-1 sm:text-lg">
          I would think that conserving our natural resources should be a
          conservative position: Not to waste food, and not to throw away a lot
          of the food that we buy.
        </p>
        <div class="mt-10 flex items-center gap-x-6">
          <a
            href="#"
            class="rounded-full shadow-[0px_8px_32px_rgba(102,107,226,0.35)] bg-primary px-3.5 py-2.5 text-sm font-medium text-white focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
            >Daftar Sekarang</a
          >
          <a
            href="#"
            class="rounded-full font-medium bg-[#f2f2f2] text-sm text-dark py-2.5 px-3.5"
            >About Us
          </a>
        </div>
      </div>
      <div class="mt-16 sm:mt-24 relative lg:mt-0 lg:shrink-0 lg:grow">
        <img
          src="@/assets/hero/main.webp"
          class="lg:mx-auto sm:w-[651px] max-w-full w-[230px]"
          alt=""
        />
        <div
          class="absolute z-20 lg:bottom-[104px] bottom-0 left-1/4 lg:-left-[109px]"
        >
          <CardReview />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import CardReview from "@/components/CardReview.vue";
</script>

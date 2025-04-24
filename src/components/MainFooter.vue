<template>
  <footer class="py-8 lg:px-10">
    <div class="px-4 bg-primary-mute pb-10 pt-20 sm:pt-24 lg:px-8">
      <div class="xl:grid xl:grid-cols-3 xl:gap-8">
        <div class="grid grid-cols-2 gap-8 xl:col-span-2">
          <div>
            <div>
              <img
                src="@/assets/logo.webp"
                alt=""
                class="h-[50px] w-auto object-contain"
              />
            </div>
            <p class="mt-6 text-sm text-light-1">
              Jl. Prof. DR. Satrio No.7, RT.3/RW.3, Karet Kuningan, Kecamatan
              Setiabudi, Kota Jakarta Selatan, Daerah Khusus Ibukota Jakarta
              12950
            </p>
            <div class="flex gap-x-6 mt-8">
              <a
                v-for="item in navigation.social"
                :key="item.name"
                :href="item.href"
                class="rounded-full size-10 bg-white flex items-center justify-center hover:bg-primary group"
              >
                <span class="sr-only">{{ item.name }}</span>
                <component
                  :is="item.icon"
                  class="size-6 group-hover:text-white"
                  aria-hidden="true"
                />
              </a>
            </div>
          </div>
          <div class="md:grid md:grid-cols-2 md:gap-8">
            <div>
              <h3 class="text-lg text-dark font-medium">Category</h3>
              <ul role="list" class="mt-6 space-y-4">
                <li v-for="item in navigation.category" :key="item.name">
                  <a
                    :href="item.href"
                    class="text-sm text-light-1 hover:text-gray-900"
                    >{{ item.name }}</a
                  >
                </li>
              </ul>
            </div>
            <div class="mt-10 md:mt-0">
              <h3 class="text-lg text-dark font-medium">About Us</h3>
              <ul role="list" class="mt-6 space-y-4">
                <li v-for="item in navigation.aboutUs" :key="item.name">
                  <a
                    :href="item.href"
                    class="text-sm text-light-1 hover:text-gray-900"
                    >{{ item.name }}</a
                  >
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="mt-10 xl:mt-0">
          <h3 class="text-lg text-dark font-medium">Newsletter</h3>
          <p class="mt-6 text-sm text-light-1">
            Get now free 50% discount for alll products on your first order
          </p>
          <form class="mt-6 flex relative sm:max-w-md">
            <input
              type="email"
              name="email-address"
              id="email-address"
              autocomplete="email"
              class="w-full min-w-0 rounded-md bg-transparent px-3 py-1.5 text-base text-black outline outline-1 -outline-offset-1 outline-black placeholder:text-gray-400 focus:outline focus:outline-2 focus:-outline-offset-2 focus:outline-indigo-600 sm:w-64 sm:text-sm/6 xl:w-full"
              placeholder="Your email address"
            />
            <div class="absolute right-0 inset-y-0 sm:shrink-0">
              <button
                type="submit"
                class="flex w-full items-center justify-center rounded-md bg-primary px-3 py-2 text-sm font-medium uppercase text-white shadow-sm focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
              >
                Send
              </button>
            </div>
          </form>
          <div class="mt-5 space-y-2.5">
            <div class="flex items-center gap-1">
              <IconEmail class="size-5 shrink-0" />
              <span class="text-sm text-black">elemesid@gmail.com</span>
            </div>
            <div class="flex items-center gap-1">
              <IconPhone class="size-5 shrink-0" />
              <span class="text-sm text-black">08811112222</span>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex justify-center text-center mt-12">
      <p class="text-sm text-light-1">
        &copy; 2021 Elemes id. All rights reserved.
      </p>
    </div>
  </footer>
</template>

<script setup lang="ts">
import IconEmail from "@/components/icons/IconEmail.vue";
import IconInstagram from "./icons/IconInstagram.vue";
import IconPhone from "./icons/IconPhone.vue";

const navigation = {
  category: [
    { name: "Cupcake", href: "#" },
    { name: "Pizza", href: "#" },
    { name: "Kebab", href: "#" },
    { name: "Salmon", href: "#" },
    { name: "Doughnut", href: "#" },
  ],
  aboutUs: [
    { name: "About Us", href: "#" },
    { name: "FAQ", href: "#" },
    { name: "Report Problem", href: "#" },
  ],
  social: [
    {
      name: "Email",
      href: "#",
      icon: IconEmail,
    },
    {
      name: "Phone",
      href: "#",
      icon: IconPhone,
    },
    {
      name: "Instagram",
      href: "#",
      icon: IconInstagram,
    },
  ],
};
</script>

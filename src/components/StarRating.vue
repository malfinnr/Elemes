<template>
  <div class="flex items-center gap-1">
    <IconStar
      v-for="index in 5"
      :key="index"
      :class="index <= filled ? 'text-orange' : 'text-[#c9c9c9]'"
    />
  </div>
</template>

<script lang="ts" setup>
import IconStar from "@/components/icons/IconStar.vue";
defineProps({
  filled: {
    type: Number,
    required: true,
  },
});
</script>

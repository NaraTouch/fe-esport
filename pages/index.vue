<script setup lang="ts">
import { TwFeather } from "vue3-tailwind";

useHead({
  title: "Dashboard",
});
</script>

<template>
  <div class="w-full">
      <ClientOnly>
        <CustomCarousel />
      </ClientOnly>
    <div class="p-4 bg-gray-100 dark:bg-gray-900 h-full">
    </div>
  </div>
</template>

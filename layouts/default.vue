<script setup lang="ts">
import { useToast, TwFeather, TwToast } from "vue3-tailwind";
const { toasts } = useToast();
const cookieDark = useCookie('dark-mode')
</script>

<template>
  <div id="dark-mode" :class="cookieDark ? 'dark vt-dark' : ''">
    <TwToast position="bottom-right" :toasts="toasts" />
    <div>
       <LayoutFloating />
      <LayoutHeader />
      <div class="px-0 md:px-1">
        <div class="flex min-h-screen text-sky-900 dark:text-gray-200 bg-opacity-40 bg-gray-900 shadow-lg">
          <slot />
        </div>
      </div>
      <div class="text-center flex items-center gap-1 justify-center text-gray-200">
        Nara AKA
        <TwFeather class="text-red-500" type="heart"/> By
        <a class="text-blue-300"
          href="https://github.com/NaraTouch"
          target="_blank">
          Wailan
        </a>
      </div>
    </div>
  </div>
</template>

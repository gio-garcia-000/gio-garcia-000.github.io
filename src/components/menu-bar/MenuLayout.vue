<template>
  <nav class="bg-gray-50 dark:bg-gray-900 py-2">
    <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto px-4 pt-4 pb-2">
      <a href="#" class="flex items-center space-x-3 rtl:space-x-reverse">
        <span class="self-center text-2xl font-bold whitespace-nowrap dark:text-red-600">Personal <span class="text-red-600 dark:text-white">Portfolio</span></span>
      </a>
      <div class="block md:hidden items-center justify-center">
        <slot name="toggle-theme"></slot>
        <slot name="toggle-button"></slot>
      </div>

      <slot name="menu-list"></slot>
      <div class="hidden md:block">
        <slot name="toggle-theme"></slot>
      </div>
    </div>
  </nav>
  <div :class="['wave', isDark ? 'wave-light' : 'wave-dark']" class="shadow-2xl" style="--size: 18px"></div>
</template>
<script setup lang="ts">
import { useDark } from '@vueuse/core'

const isDark = useDark()
</script>

<style scoped>
.wave {
  --size: 50px;
  --R: calc(var(--size) * 1.28);
  height: 40px;
  width: 100%;
  transform: rotate(180deg);
  z-index: 10;
  position: absolute;
}

.wave-light {
  background: #111827; /* Dark background for light mode */
  -webkit-mask:
    radial-gradient(var(--R) at 50% calc(1.8 * var(--size)), #fff 99%, #0000 101%) calc(50% - 2 * var(--size)) 0 / calc(4 * var(--size)) 100%,
    radial-gradient(var(--R) at 50% calc(-0.8 * var(--size)), #0000 99%, #fff 101%) 50% var(--size) / calc(4 * var(--size)) 100% repeat-x;
}

.wave-dark {
  background: #f9fafb; /* Light background for dark mode */
  -webkit-mask:
    radial-gradient(var(--R) at 50% calc(1.8 * var(--size)), #000 99%, #0000 101%) calc(50% - 2 * var(--size)) 0 / calc(4 * var(--size)) 100%,
    radial-gradient(var(--R) at 50% calc(-0.8 * var(--size)), #0000 99%, #000 101%) 50% var(--size) / calc(4 * var(--size)) 100% repeat-x;
}
</style>

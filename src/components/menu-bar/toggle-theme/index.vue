<script setup lang="ts">
import { useDark, useToggle } from '@vueuse/core'

const isDark = useDark()
const toggleDarkMode = useToggle(isDark)
</script>

<template>
  <label class="inline-flex items-center cursor-pointer">
    <input type="checkbox" class="sr-only peer" v-model="isDark" @click="toggleDarkMode()" />
    <div
      class="relative w-11 h-6 bg-gray-200 peer-focus:outline-none peer-focus:ring-2 peer-focus:ring-blue-300 dark:peer-focus:ring-blue-800 rounded-full peer dark:bg-gray-700 peer-checked:after:translate-x-full rtl:peer-checked:after:-translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:start-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all dark:border-gray-600 peer-checked:bg-rose-600"
    ></div>
    <span class="sr-only">Switch to light / dark version</span>
  </label>
</template>

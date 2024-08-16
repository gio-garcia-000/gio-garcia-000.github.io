<script setup lang="ts">
import AboutLayout from '@/components/about-me/AboutLayout.vue'
import FrontEndIcon from '@/components/icons/FrontEndIcon.vue'
</script>
<template>
  <AboutLayout>
    <template #main-text>
      <h1 class="max-w-2xl mb-4 text-3xl font-extrabold tracking-tight leading-none md:text-4xl xl:text-5xl dark:text-white">My <span class="text-red-600">Services</span></h1>
      <p class="max-w-xl mb-6 font-light text-gray-500 lg:mb-8 md:text-lg lg:text-base dark:text-gray-400">
        Greetings, fellow digital explorers! I am Gio Garcia, a passionate and innovative developer dedicated to crafting immersive digital experiences. Welcome to my online abode.
      </p>
    </template>
    <template #box>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div class="grid grid-rows-2 gap-8">
          <div class="bg-card dark:bg-gradient-to-r from-red-500/40 to-rose-500/40 px-8 py-10 rounded-sm border-2 border-rose-600/70 shadow-md">
            <div class="flex justify-center items-center mb-4">
              <FrontEndIcon />
            </div>
            <h3 class="text-xl font-semibold mb-2 text-slate-900 dark:text-white text-center">Frontend Develop</h3>
            <p class="text-muted-foreground text-sm dark:text-slate-300 text-center">Greetings, fellow digital explorers! I am Gio Garcia, a passionate developer.</p>
          </div>
          <div class="bg-card dark:bg-gradient-to-r from-red-500/40 to-rose-500/40 px-8 py-10 rounded-sm border-2 border-rose-600/70 shadow-md">
            <div class="flex justify-center items-center mb-4">
              <FrontEndIcon />
            </div>
            <h3 class="text-xl font-semibold mb-2 text-slate-900 dark:text-white text-center">Right Develop</h3>
            <p class="text-muted-foreground text-sm dark:text-slate-300 text-center">Greetings, fellow digital explorers! I am Gio Garcia, a passionate developer.</p>
          </div>
        </div>
        <div class="grid grid-rows-2 md:row-span-2 md:mt-8 gap-8">
          <div class="bg-card dark:bg-gradient-to-r from-red-500/40 to-rose-500/40 px-8 py-10 rounded-sm border-2 border-rose-600/70 shadow-md">
            <div class="flex justify-center items-center mb-4">
              <FrontEndIcon />
            </div>
            <h3 class="text-xl font-semibold mb-2 text-slate-900 dark:text-white text-center">Backend Develop</h3>
            <p class="text-muted-foreground text-sm dark:text-slate-300 text-center">Greetings, fellow digital explorers! I am Gio Garcia, a passionate developer.</p>
          </div>
          <div class="bg-card dark:bg-gradient-to-r from-red-500/40 to-rose-500/40 px-8 py-10 rounded-sm border-2 border-rose-600/70 shadow-md">
            <div class="flex justify-center items-center mb-4">
              <FrontEndIcon />
            </div>
            <h3 class="text-xl font-semibold mb-2 text-slate-900 dark:text-white text-center">Bottom Develop</h3>
            <p class="text-muted-foreground text-sm dark:text-slate-300 text-center">Greetings, fellow digital explorers! I am Gio Garcia, a passionate developer.</p>
          </div>
        </div>
      </div>
    </template>
  </AboutLayout>
</template>

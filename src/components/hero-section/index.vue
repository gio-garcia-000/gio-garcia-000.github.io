<script setup lang="ts">
import HeroImage from '../../assets/images/hero/hero-gio.png'
import HeroLayout from '@/components/hero-section/HeroLayout.vue'
const imageSrc = HeroImage
</script>

<template>
  <HeroLayout>
    <template #main-text>
      <h1 class="max-w-2xl mb-4 text-4xl font-extrabold tracking-tight leading-none md:text-5xl xl:text-6xl dark:text-white">I'M <span class="text-red-600">DEVELOPER</span></h1>
      <h1 class="max-w-2xl mb-4 text-4xl font-extrabold tracking-tight leading-none md:text-5xl xl:text-6xl dark:text-white">GIO GARCIA</h1>
      <p class="max-w-2xl mb-6 font-light text-gray-500 lg:mb-8 md:text-lg lg:text-base dark:text-gray-400">
        I'm Gio Garcia, a developer with a passion for learning and a drive to tackle new challenges. Although I don't have formal work experience yet, my enthusiasm and commitment to growth are at the core of my journey. I'm eager to apply my
        skills, explore new technologies, and contribute to exciting projects.
      </p>
    </template>
    <template #image-hero>
      <img :src="imageSrc" alt="mockup" class="w-full h-auto" />
    </template>
  </HeroLayout>
</template>

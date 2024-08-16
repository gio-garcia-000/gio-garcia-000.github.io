<script setup lang="ts">
import MenuBar from '@/components/menu-bar/index.vue'
import HeroSection from '@/components/hero-section/index.vue'
import AboutMe from '@/components/about-me/index.vue'
</script>

<template>
  <div class="min-h-screen dark:bg-gray-900 transition-colors duration-1000">
    <MenuBar />
    <HeroSection />
    <AboutMe/>
  </div>
</template>

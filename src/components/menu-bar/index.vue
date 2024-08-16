<script setup lang="ts">
import ToggleTheme from '@/components/menu-bar/toggle-theme/index.vue'
import BurgerIcon from '@/components/icons/BurgerIcon.vue'
import MenuLayout from '@/components/menu-bar/MenuLayout.vue'
import { reactive, ref } from 'vue'

const navItems = reactive([
  { name: 'About Me', href: '#about' },
  { name: 'Projects', href: '#projects' },
  { name: 'Contact', href: '#contact' }
])
const isNavbarOpen = ref<boolean>(false)
const toggleNavbar = () : void => {
  isNavbarOpen.value = !isNavbarOpen.value
}
</script>

<template>
  <MenuLayout>
    <template #toggle-theme>
      <ToggleTheme />
    </template>
    <template #toggle-button>
      <button
        @click="toggleNavbar"
        type="button"
        class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
        aria-controls="navbar-solid-bg"
        aria-expanded="false"
      >
        <span class="sr-only">Open main menu</span>
        <BurgerIcon />
      </button>
    </template>
    <template #menu-list>
      <div :class="{ hidden: !isNavbarOpen, 'w-full': true, 'md:block': true, 'md:w-auto': true }">
        <ul class="flex flex-col font-thin gap-2 mt-4 rounded-lg bg-gray-50 md:space-x-8 rtl:space-x-reverse md:flex-row md:mt-0 md:border-0 md:bg-transparent dark:bg-gray-800 md:dark:bg-transparent dark:border-gray-700">
          <li v-for="navItem in navItems">
            <a href="#" class="block py-2 px-3 md:p-0 text-slate-950 dark:text-white hover:text-red-500 rounded md:bg-transparent md:text-slate-950 md:dark:text-white" aria-current="page">{{ navItem.name }}</a>
          </li>
        </ul>
      </div>
    </template>
  </MenuLayout>
</template>

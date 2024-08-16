<template>
  <section class="relative bg-white dark:bg-gradient-to-r from-slate-800 to-orange-800">
    <div class="grid max-w-screen-xl px-4 py-28 mx-auto md:py-0 md:gap-8 lg:gap-8 xl:gap-0 lg:grid-cols-12">
      <div class="mr-auto place-self-center lg:col-span-7">
        <slot name="main-text"></slot>
      </div>
      <div class="hidden lg:mt-0 lg:col-span-5 lg:flex">
        <slot name="image-hero"></slot>
      </div>
    </div>
  </section>
</template>

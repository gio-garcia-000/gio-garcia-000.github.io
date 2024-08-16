<template>
    <section class="bg-white dark:bg-gray-900 py-20">
      <div class="grid max-w-screen-xl px-4 pt-5 mx-auto lg:gap-8 xl:gap-0 lg:grid-cols-12">
        <div class="mr-auto place-self-center lg:col-span-7">
          <slot name="main-text"></slot>
        </div>
        <div class="lg:mt-0 lg:col-span-5">
          <slot name="box"></slot>
        </div>
      </div>
    </section>
  </template>
  
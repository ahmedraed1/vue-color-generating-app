<template>
  <div class="flex flex-col">
    <div class="w-64 h-48 bg-white"></div>
    <div>
      <ul class="flex flex-row justify-center w-full my-2">
        <li class="w-full h-8 hover:scale-125 bg-white text-black"></li>
        <li class="w-full h-8 hover:scale-125 bg-white text-black"></li>
        <li class="w-full h-8 hover:scale-125 bg-white text-black"></li>
        <li class="w-full h-8 hover:scale-125 bg-white text-black"></li>
      </ul>
    </div>
    <div class="flex flex-row justify-between">
      <button
        type="button"
        class="inline-block rounded bg-neutral-800 px-6 pb-2 pt-2.5 text-xs font-medium uppercase leading-normal text-neutral-50 shadow-dark-3 transition duration-150 ease-in-out hover:bg-neutral-700 hover:shadow-dark-2 focus:bg-neutral-700 focus:shadow-dark-2 focus:outline-none focus:ring-0 active:bg-neutral-900 active:shadow-dark-2 motion-reduce:transition-none dark:shadow-black/30 dark:hover:shadow-dark-strong dark:focus:shadow-dark-strong dark:active:shadow-dark-strong"
      >
        A
      </button>
      <button
        type="button"
        class="inline-block rounded bg-neutral-800 px-6 pb-2 pt-2.5 text-xs font-medium uppercase leading-normal text-neutral-50 shadow-dark-3 transition duration-150 ease-in-out hover:bg-neutral-700 hover:shadow-dark-2 focus:bg-neutral-700 focus:shadow-dark-2 focus:outline-none focus:ring-0 active:bg-neutral-900 active:shadow-dark-2 motion-reduce:transition-none dark:shadow-black/30 dark:hover:shadow-dark-strong dark:focus:shadow-dark-strong dark:active:shadow-dark-strong"
      >
        B
      </button>
      <button
        type="button"
        class="inline-block rounded bg-neutral-800 px-6 pb-2 pt-2.5 text-xs font-medium uppercase leading-normal text-neutral-50 shadow-dark-3 transition duration-150 ease-in-out hover:bg-neutral-700 hover:shadow-dark-2 focus:bg-neutral-700 focus:shadow-dark-2 focus:outline-none focus:ring-0 active:bg-neutral-900 active:shadow-dark-2 motion-reduce:transition-none dark:shadow-black/30 dark:hover:shadow-dark-strong dark:focus:shadow-dark-strong dark:active:shadow-dark-strong"
      >
        C
      </button>
    </div>
    <div class="my-2">
      <span class="block text-xl">HEX: <span class="text-white">#07485B</span> </span>
      <span class="block text-xl">RGB: <span class="text-white">7, 72, 91</span> </span>
      <span class="block text-xl"
        >HSL: <span class="text-white">193.57, 85.71%, 19.22%</span>
      </span>
    </div>
  </div>
</template>
<script setup></script>
<style scoped>
div > ul {
  list-style: none;
}
</style>

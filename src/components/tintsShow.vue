<template>
  <div>
    <h1>Tints</h1>
    <div class="bg-black py-8 flex flex-row gap-6">
      <div class="w-1/2 flex flex-row items-end gap-2">
        <form class="max-w-xs mx-auto">
          <label
            for="quantity-input"
            class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
            >Steps:</label
          >
          <div class="relative flex items-center max-w-[8rem]">
            <button
              type="button"
              id="decrement-button"
              data-input-counter-decrement="quantity-input"
              class="bg-gray-100 dark:bg-gray-700 dark:hover:bg-gray-600 dark:border-gray-600 hover:bg-gray-200 border border-gray-300 rounded-s-lg p-3 h-11 focus:ring-gray-100 dark:focus:ring-gray-700 focus:ring-2 focus:outline-none"
              @click="decrement"
            >
              <svg
                class="w-3 h-3 text-gray-900 dark:text-white"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 18 2"
              >
                <path
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M1 1h16"
                />
              </svg>
            </button>
            <input
              type="text"
              id="quantity-input"
              data-input-counter
              aria-describedby="helper-text-explanation"
              class="bg-gray-50 border-x-0 border-gray-300 h-11 text-center text-gray-900 text-sm focus:ring-blue-500 focus:border-blue-500 block w-full py-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
              placeholder="999"
              required
              v-model="steps"
            />
            <button
              type="button"
              id="increment-button"
              data-input-counter-increment="quantity-input"
              class="bg-gray-100 dark:bg-gray-700 dark:hover:bg-gray-600 dark:border-gray-600 hover:bg-gray-200 border border-gray-300 rounded-e-lg p-3 h-11 focus:ring-gray-100 dark:focus:ring-gray-700 focus:ring-2 focus:outline-none"
              @click="increment"
            >
              <svg
                class="w-3 h-3 text-gray-900 dark:text-white"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 18 18"
              >
                <path
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M9 1v16M1 9h16"
                />
              </svg>
            </button>
          </div>
        </form>
        <input
          id="default-range"
          type="range"
          v-model="steps"
          @change="yep"
          class="w-1/2 h-2 bg-gray-200 rounded-lg appearance-none cursor-pointer dark:bg-gray-700 mb-5"
        />
      </div>
      <!-- <div>
        <label
          for="quantity-input"
          class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
          >Mode::</label
        >
      </div> -->
    </div>
    <div>
      <ul>
        <li class="w-44 h-52 px-2 mt-4 float-left" v-for="(item, index) in steps" :key="index">
          <div class="w-full h-1/2 bg-white"></div>
          <div class="p-2">
            <span class="block text-xs">HEX: <span class="text-white">#07485B</span> </span>
            <span class="block text-xs">RGB: <span class="text-white">7, 72, 91</span> </span>
            <span class="block text-xs"
              >HSL: <span class="text-white">193.57, 85.71%, 19.22%</span>
            </span>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>
<script setup>
import { ref } from 'vue'

const steps = ref(6)

const increment = () => (steps.value = parseInt(steps.value) + 1)
const decrement = () => (steps.value -= 1)

const yep = () => {
  steps.value = parseInt(steps.value)
}
</script>
<style scoped>
div > ul {
  list-style: none;
}
</style>

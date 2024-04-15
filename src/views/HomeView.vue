<template>
  <main class="flex h-full">
    <div class="flex flex-row w-full">
      <colorShow />
      <div class="flex flex-col pl-2 w-full">
        <tintsShow />
      </div>
    </div>
  </main>
</template>
<script setup>
import colorShow from '../components/colorShow.vue'
import tintsShow from '../components/tintsShow.vue'
</script>

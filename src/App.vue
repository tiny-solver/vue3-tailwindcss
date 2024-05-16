<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { onMounted } from 'vue';
import { initFlowbite } from 'flowbite';

// initialize components based on data attribute selectors
onMounted(() => {
  initFlowbite();
})
</script>

<template>
  <header>
    <div class="p-2 rounded-xl bg-red-400 text-black font-bold">Hello My Vue3 + Tailwindcss in container</div>
  </header>

  <RouterView />
</template>

<style scoped></style>

<script setup lang="ts">
import { RouterView } from 'vue-router'
import Toaster from '@/components/ui/toast/Toaster.vue'
import { useColorMode } from '@vueuse/core'
import TheHeader from './components/TheHeader.vue'
const mode = useColorMode()
</script>

<template>
  <Toaster />
  <TheHeader />

  <main class="center-content-grid">
    <RouterView />
  </main>
</template>

<style scoped>
.center-content-grid {
  display: grid;
  place-items: center;
  height: 80vh;
}
</style>

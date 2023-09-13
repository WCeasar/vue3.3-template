<script setup lang="ts">
import { RouterLink } from 'vue-router/auto'
import { registerSW } from 'virtual:pwa-register'

const updateSW = registerSW({
  immediate: true,
  onNeedRefresh() {
    console.log('更新')
  },
  onRegisteredSW(url, registration) {
    setInterval(() => {
      registration?.update()
    })
  }
})

onMounted(() => {
  updateSW()
})
const target = ref<HTMLDivElement>()
</script>

<template>
  <div class="index-page">
    <div class="bg-yellow-300 h-11 w-11" ref="target"></div>
  </div>

  <i-mdi-account class="font-medium text-red-400" />

  <router-link to="/about">about</router-link>
</template>

<style lang="scss" scoped></style>

<route lang="yaml">
meta:
  layout: layout
</route>

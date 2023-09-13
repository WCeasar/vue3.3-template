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
    }, 36000)
  }
})

onMounted(() => {
  updateSW()
})
</script>

<template>
  <div>
    index
    <router-link to="/about">about</router-link>
  </div>
</template>

<style lang="scss" scoped></style>

<route lang="yaml">
meta:
  layout: default
</route>

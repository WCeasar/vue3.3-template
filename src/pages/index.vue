<script setup lang="ts">
import { RouterLink } from 'vue-router/auto'

const target = ref<HTMLDivElement>()
</script>

<template>
  <div class="index-page">
    <HelloWorld name="12"></HelloWorld>

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

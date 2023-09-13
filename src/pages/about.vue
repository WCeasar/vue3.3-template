<script setup lang="ts">
import { RouterLink } from 'vue-router/auto'
</script>

<template>
  <div class="about-page">about</div>
  <!-- A basic anchor icon from Phosphor icons -->
  <div class="i-ph-anchor-simple-thin" />
  <!-- An orange alarm from Material Design Icons -->
  <div class="i-mdi-alarm text-orange-400" />
  <!-- A large Vue logo -->
  <div class="i-logos-vue text-3xl" />
  <!-- Sun in light mode, Moon in dark mode, from Carbon -->
  <button class="i-carbon-sun dark:i-carbon-moon" />
  <button class="i-ph:airplane-tilt-duotone text-9xl" />
  <!-- Twemoji of laugh, turns to tear on hovering -->
  <router-link to="/">index</router-link>
</template>

<style lang="scss" scoped></style>

<route lang="yaml">
meta:
  layout: home
</route>

<script setup lang="ts"></script>

<template>
  <div class="404-page">404</div>
  <RouterView></RouterView>
  <button @click="$router.back()">点击返回</button>
</template>

<style lang="scss" scoped></style>

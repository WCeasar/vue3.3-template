<script setup lang="ts">
defineOptions({
  name: 'DE1MO'
})

const emits = defineEmits<{ customClick: [num: number] }>()

const number = ref<number>(1)
const handleClick = () => {
  emits('customClick', number.value++)
  console.log('click')
}
</script>

<template>
  <div class="-page">
    <div>Demo</div>
    <button @click="handleClick">click me</button>
  </div>
</template>

<style lang="scss" scoped></style>

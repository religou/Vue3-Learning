<template>
  <div>这是子组件</div>
  <span>父组件传来的数据：{{ props.count }}</span>
</template>

<script setup>
const props = defineProps(['count'])
</script>

<style scoped></style>

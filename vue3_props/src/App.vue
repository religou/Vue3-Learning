<template>
  <div class="parent">
    <h3>这是父组件</h3>
    <Son :count="count"></Son>
    <button @click="add">父组件中的增加</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Son from './components/Son.vue'

const count = ref(0)

function add() {
  count.value++
}
</script>

<style scoped></style>

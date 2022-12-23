<template>
  <div class="tab-wrapper">
    <div class="tab-head">
      <div
        class="tab-button"
        :class="{ active: current === 0 }"
        @click="current = 0"
      >
        球员
      </div>
      <div
        class="tab-button"
        :class="{ active: current === 1 }"
        @click="current = 1"
      >
        球队
      </div>
    </div>

    <div class="tab-body"></div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const current = ref(0)
</script>

<style scoped>
.tab-wrapper {
  /* 加了这个，padding不会影响设置的宽度和高度 */
  box-sizing: border-box;
  width: 800px;
  padding: 20px;
  background-color: rgb(45, 82, 212);
}

.tab-head {
  display: flex;
  overflow: hidden;
  border-radius: 5px;
}

.tab-button {
  font-size: 20px;
  text-align: center;
  padding: 5px 0;
  background-color: #fff;
  flex: auto;
  cursor: pointer;
}

.active {
  color: #fff;
  background-color: rgb(188, 2, 53);
}
</style>

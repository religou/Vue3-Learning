
<template>
  <!-- 使用 v-if 直接隐藏元素 -->
  <div v-if="if_flag">
    使用v-if需要显示的区域
  </div>

  <div v-if="!if_flag">
    使用v-if不需要显示的区域
  </div>

  <!-- 使用v-show 设置元素的display属性，工作中更频繁使用v-show，更加节省资源 -->
  <div v-show="show_flag">
    使用v-show需要显示的区域
  </div>

  <div v-show="!show_flag">
    使用v-show不需要显示的区域
  </div>

  <!-- 使用 v-on 来添加事件触发器，工作中更频繁使用 @, 节约代码空间 -->
  <!-- <button v-on:click="showInfo">点击触发事件</button> -->
  <button @click="showInfo">点击触发事件</button><br>

  <input type="text" v-model="name">
  <div>
    {{ name }}
  </div>

  <div v-for="item in arr">
    {{item}}
  </div>
</template>

<script setup lang="ts">
import { ref, Ref } from 'vue';

const if_flag: boolean = true;

const show_flag: boolean = true;

const showInfo = () => {
  console.log("触发了事件")
}

const name = ref("姓名");

const arr:Array<string> = ["1", "2", "3", "4"];
</script>


<style scoped>
</style>

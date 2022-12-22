<template>
  <div>
    <div class="msg">
      {{ p1 }}
    </div>
    <button>修改</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref, reactive, onMounted, watch } from 'vue'

export default defineComponent({
  setup() {
    interface Member {
      id: number
      name: string
      gender: number
      age: number
    }

    const p1 = reactive({
      id: 1,
      name: '张三',
      gender: 0,
      age: 24,
    })

    setTimeout(() => {
      p1.age += 1
    }, 3000)

    watch(p1, (newValue, oldValue) => {
      console.log('变更前的值：' + oldValue.age + ', 变更后的值：' + newValue.age)
    })

    return {
      p1,
    }
  },
})
</script>

<style scoped>
.msg {
  font-size: 14px;
}
</style>

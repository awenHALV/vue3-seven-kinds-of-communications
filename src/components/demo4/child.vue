
<template>
  <div class="input-wrap">
    <input
      v-model="value"
      type="text"
      class="form-control"
      placeholder="请输入"
    />
    <div class="input-group-appaned">
      <button
        type="button"
        class="btn btn-primary"
        @click="handleAdd"
      > 添加</button>
    </div>
  </div>
</template>

<script setup>
import { ref, defineExpose } from 'vue'
const list = ref(['JavaScript', 'HTML', 'CSS'])
const value = ref('')
// add 触发后的事件处理函数
const handleAdd = () => {
  list.value.push(value.value)
  value.value = ''
}
// 为了使组件外部能够通过访问到，需要将其暴露出去
defineExpose({ list })
</script>

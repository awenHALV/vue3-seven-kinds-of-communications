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
import { ref, defineEmits } from 'vue';
const value = ref('');
const emits = defineEmits(['add']);
const handleAdd = () => {
  emits('add', value.value);
  value.value = '';
}
</script>

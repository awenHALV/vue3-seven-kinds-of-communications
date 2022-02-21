<template>
  <div>
    <!--子组件-->
    <child-component></child-component>
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
  </div>
</template>

<script setup>
import { ref, provide, readonly } from 'vue';
import ChildComponent from '../../components/demo5/child.vue';
const list = ref(['JavaScript', 'HTML', 'CSS']);
const value = ref('');
// 向子组件提供数据
provide('list', readonly(list.value))
const handleAdd = () => {
  list.value.push(value.value);
  value.value = '';
}
</script>

<style scoped>
</style>
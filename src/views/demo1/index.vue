<template>
  <div>
    <!--子组件-->
    <child-component :list="list"></child-component>
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
import { ref } from 'vue';
import ChildComponent from '../../components/demo1/Child.vue';
const list = ref(['JavaScript', 'HTML', 'CSS']);
const value = ref('');
const handleAdd = () => {
  list.value.push(value.value);
  value.value = '';
}
</script>

<style scoped>
</style>
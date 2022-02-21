<template>
  <ul class="parant list-group">
    <li
      :key="i"
      class="list-group-item"
      v-for="i in list"
    >{{i}}</li>
  </ul>
  <childComponent @add="handelAdd"></childComponent>
</template>

<script setup>
import { ref } from 'vue';
import childComponent from '../../components/demo2/child.vue';
const list = ref(['JavaScript', 'HTML', 'CSS']);
const handelAdd = (value) => {
  list.value.push(value);
}
</script>

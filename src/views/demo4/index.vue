<template>
  <ul class="parant list-group">
    <li
      :key="i"
      class="list-group-item"
      v-for="i in childRefs?.list"
    >{{i}}</li>
  </ul>
  <!--通过ref可访问到组件内部暴露出来的属性-->
  <childComponent ref="childRefs"></childComponent>
</template>

<script setup>
import { ref } from 'vue';
import childComponent from '../../components/demo4/child.vue';
const childRefs = ref(null);
</script>

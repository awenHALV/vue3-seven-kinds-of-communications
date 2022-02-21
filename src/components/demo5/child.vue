<template>
  <ul class="parant list-group">
    <li
      :key="i"
      class="list-group-item"
      v-for="i in list"
    >{{i}}</li>
  </ul>
</template>

<script setup>
import { inject } from 'vue';
const list = inject('list');
</script>

<style scoped>
</style>
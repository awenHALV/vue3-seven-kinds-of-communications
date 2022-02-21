<template>
  <ul class="parant list-group">
    <li
      :key="i"
      class="list-group-item"
      v-for="i in props.list"
    >{{i}}</li>
  </ul>
</template>

<script setup>
import { defineProps } from 'vue';
const props = defineProps({
  list: {
    type: Array,
    default: () => []
  }
})
</script>

<style scoped>
</style>
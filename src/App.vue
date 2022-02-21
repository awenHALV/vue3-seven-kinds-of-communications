<template>
  <!--props方式-->
  <p>props方式</p>
  <demo1></demo1>
  <!--emit方式-->
  <p>emit方式</p>
  <demo2></demo2>
  <!--v-model方式-->
  <p>v-model方式</p>
  <demo3></demo3>
  <!--refs方式-->
  <p>refs方式</p>
  <demo4></demo4>
  <p>provide/inject方式</p>
  <demo5></demo5>
  <p>EventBus事件总线（不推荐）(推荐mitt或者tiny-emitter)</p>
  <p>状态管理工具（Vuex/pinia）</p>
</template>

<script>
import Demo1 from './views/demo1/index.vue';
import Demo2 from './views/demo2/index.vue';
import Demo3 from './views/demo3/index.vue';
import Demo4 from './views/demo4/index.vue';
import Demo5 from './views/demo5/index.vue';
export default {
  name: 'App',
  components: {
    Demo1,
    Demo2,
    Demo3,
    Demo4,
    Demo5
  }
}
</script>

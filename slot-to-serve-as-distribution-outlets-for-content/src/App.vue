<template>
  <!-- 字符串 -->
  <HelloWorld msg="slot-to-serve-as-distribution-outlets-for-content">
    Hello
  </HelloWorld>

  <!-- HTML -->
  <HelloWorld msg="slot-to-serve-as-distribution-outlets-for-content">
    <a href="https://geool.xyz">Welcome to geool.xyz</a>
  </HelloWorld>

  <!-- 模板 -->
  <HelloWorld msg="slot-to-serve-as-distribution-outlets-for-content">
    <div id="counter">Counter: {{ counter }}</div>
  </HelloWorld>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import HelloWorld from './components/HelloWorld.vue';

@Options({
  components: {
    HelloWorld,
  },
})
export default class App extends Vue {
  private counter: number = 0;
}
</script>

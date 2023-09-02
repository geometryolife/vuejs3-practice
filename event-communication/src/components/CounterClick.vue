<template>
  <div class="hello">
    <button v-on:click="plusOne">递增</button>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  emits: ["plusOneEvent"],
})
export default class HelloWorld extends Vue {
  // 定义一个组件方法
  plusOne() {
    console.log("emit event");

    // 发送自定义事件
    this.$emit("plusOneEvent");
  }
}
</script>

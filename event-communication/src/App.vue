<template>
  <CounterClick @plusOneEvent="handlePlusOneEvent" />
  <CounterShow :count="counter" />
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import CounterClick from './components/CounterClick.vue';
import CounterShow from './components/CounterShow.vue';

@Options({
  components: {
    CounterClick,
    CounterShow
  },
})
export default class App extends Vue {
  // eslint-disable-next-line
  private counter: number = 0;

  handlePlusOneEvent() {
    console.log("handlePlusOneEvent");

    // 计数器进行递增操作
    this.counter++;
  }
}
</script>

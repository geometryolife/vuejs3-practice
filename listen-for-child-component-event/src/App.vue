<template>
  <HelloWorld
  msg="listen-for-child-component-event"
  @plusOneEvent="handlePlusOneEvent"
/>
  <div id="counter">Counter: {{ counter }}</div>
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
  // eslint-disable-next-line
  private counter: number = 0;

  handlePlusOneEvent() {
    console.log("handlePlusOneEvent");

    // 计数器进行递增操作
    this.counter++;
  }
}
</script>

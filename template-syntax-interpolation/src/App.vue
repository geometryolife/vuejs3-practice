<template>
    <!-- 文本插值 -->
    <h1>{{ msg }}</h1>

    <!-- 使用 v-once 指令来执行一次性地插值 -->
    <h1 v-once>{{ msg }}</h1>

    <!-- 输出原生的 HTML，需要使用 v-html 指令 -->
    <p>未使用 v-html 指令: {{ rawHtml }}</p>
    <p>使用 v-html 指令: <span v-html="rawHtml"></span></p>

    <!-- 绑定 HTML attribute -->
    <div v-bind:id="dynamicId"></div>

    <!-- 绑定布尔 attribute -->
    <button v-bind:disabled="isButtonDisabled">Button</button>

    <!-- JavaScript 表达式 -->
    <p>运算: {{ age + 1 }}</p>
    <p>三元表达式: {{ areYouOk ? "YES" : "NO" }}</p>
    <p>字符串操作: {{ message.split("").reverse().join("") }}</p>
    <div v-bind:id="'list-' + listId"></div>
</template>

<script lang="ts">
import { Vue } from 'vue-class-component';

export default class App extends Vue {
  private msg: string = "template-syntax-interpolation";
  private rawHtml: string = `<a href="https://waylau.com/">Welcome to geool.xyz</a>`;
  private dynamicId: number = 123;
  private isButtonDisabled: boolean = true;
  private age: number = 33;
  private areYouOk: boolean = false;
  private message: string =
    "战实发开用应级业企 sj.edoN 战实发开与析解理原 ytteN 战实构架级量轻用应网联互型大 战实发开用应级业企 ralugnA 析分例案及术技用常统系式布分";
  private listId: number = 111;
}
</script>

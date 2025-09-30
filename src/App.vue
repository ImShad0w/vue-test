<script setup>
import { ref } from "vue";

const hideText = ref(false);

import counterWithMsg from './counterWithMsg.vue';
import hideTextVue from './hideText.vue';
import showTextBelow from "./showTextBelow.vue";
import listRendering from './listRendering.vue';

</script>
<template>
  <h1>Excercises with Vue.js</h1>
  <h2>Counter with a special message!</h2>
  <counterWithMsg />
  <h2 :class="hideText ? 'hidden' : 'red'">Button that hides and unhides some text</h2>
  <hideTextVue @response="(msg) => hideText = msg" />
  <h2>Input that underneath shows current text</h2>
  <showTextBelow />
  <h2>List with delete buttons</h2>
  <listRendering />
</template>
<style>
.hidden {
  display: none;
}

.red {
  color: red;
}
</style>

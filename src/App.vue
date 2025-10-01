<script setup>
import { ref } from "vue";

const hideText = ref(false);

import counterWithMsg from './counterWithMsg.vue';
import hideTextVue from './hideText.vue';
import showTextBelow from "./showTextBelow.vue";
import listRendering from './listRendering.vue';
import counterLimit from "./counterLimit.vue";
import textReverser from "./textReverser.vue";
import passwordHider from "./passwordHider.vue";
import dynamicClassSwitcher from "./dynamicClassSwitcher.vue";
import dropDownList from "./dropDownList.vue";
import characterCounter from "./characterCounter.vue";
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
  <h2>Counter with limit</h2>
  <counterLimit />
  <h2>Text reverser</h2>
  <textReverser />
  <h2>Password hider</h2>
  <passwordHider />
  <h2>Dynamic class switcher</h2>
  <dynamicClassSwitcher />
  <h2>Dropdown list showing the current selection</h2>
  <dropDownList />
  <h2>Character counter</h2>
  <characterCounter />
</template>
<style>
.hidden {
  display: none;
}

.red {
  color: red;
}
</style>

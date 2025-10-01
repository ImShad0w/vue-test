<script setup>
import { ref } from "vue";
const text = ref("");
function reverseText() {
  text.value = text.value.split("").reverse().join("");
}
</script>
<template>
  <input v-model="text"></input>
  <button @click="reverseText">Reverse the text</button>
  <h4>Reversed text:</h4>
  <p>{{ text }}</p>
</template>

<script setup>
import { ref } from "vue";
const inpText = ref("");
const text = ref("");
function getText() {
  text.value = inpText;
}
</script>
<template>
  <input v-model="inpText" placeholder="write some shit" required></input>
  <button @click="getText">Show text below</button>
  <p>{{ text }}</p>
</template>

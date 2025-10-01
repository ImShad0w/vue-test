<script setup>
import { ref } from "vue";

const counter = ref(0);

function increment() {
  counter.value++
}

function resetCount() {
  counter.value = 0;
}

</script>
<template>
  <p>{{ counter }}</p>
  <button @click="increment" :disabled="counter == 10">{{ counter == 10 ? "Limit reached!" : "+" }}</button>
  <button @click="resetCount">Reset the count</button>
</template>

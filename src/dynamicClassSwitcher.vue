<script setup>
import { ref } from "vue";
const color = ref("");
</script>
<template>
  <p :class="color">This is some text</p>
  <button @click="color = 'red'">Make me red</button>
  <button @click="color = 'green'">Make me green</button>
  <button @click="color = 'blue'">Make me blue</button>
</template>
<style>
.red {
  color: red;
}

.green {
  color: green;
}

.blue {
  color: blue;
}
</style>

<script setup>
import { ref } from "vue";
const selected = ref("");
let id = 0;
const options = ref([
  { id: id++, text: "Dog" },
  { id: id++, text: "Cat" },
  { id: id++, text: "Frog" },
])
</script>
<template>
  <select v-model="selected">
    <option v-for="option in options" :id="option.id">
      {{ option.text }}
    </option>
  </select>
  <p>{{ selected }}</p>
</template>

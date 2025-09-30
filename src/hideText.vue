<script setup>
import { ref } from "vue";
const emit = defineEmits(["response"]);
const hideElement = ref(false)
function toggle() {
  hideElement.value = !hideElement.value
  emit("response", hideElement.value);
}
</script>
<template>
  <button @click="toggle">{{ hideElement ? "Hidding the text" : "Not hidding the text" }}</button>
</template>

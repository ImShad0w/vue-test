<script setup>
import { ref } from "vue";
const password = ref("");
const hide = ref(false);
function toggle() {
  hide.value = !hide.value
}
</script>
<template>
  <input v-model="password" :type="[hide ? 'password' : 'text']"></input>
  <button @click="toggle">Toggle pass visibility</button>
</template>

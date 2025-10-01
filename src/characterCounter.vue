<script setup>
import { ref, computed } from 'vue';
const text = ref("");
const len = computed(() => text.value.length);
</script>
<template>
  <input v-model="text"></input>
  <p>{{ len }}</p>
</template>

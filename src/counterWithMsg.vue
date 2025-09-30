<script setup>
import { ref } from "vue"

const count = ref(0)

function increment() {
  count.value++;
}

function decrement() {
  count.value--;
}
</script>

<template>
  <h1>{{ count }}</h1>
  <p v-if="count < 0">Below zero!</p>
  <p v-else-if="count === 0">Zero!</p>
  <p v-else="count > 0">Positive!</p>
  <button @click="decrement">-</button>
  <button @click="increment">+</button>
</template>

<style scoped></style>

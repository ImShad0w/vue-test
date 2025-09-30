<script setup>
import { ref } from "vue";
let id = 0;

const items = ref([])

const newItem = ref("");

function deleteItem(item) {
  items.value = items.value.filter((i) => i != item);
}

function addItem() {
  items.value.push({ id: id++, title: newItem.value });
  newItem.value = "";
}

</script>
<template>
  <input v-model="newItem"></input>
  <button @click="addItem">Create...</button>
  <ul>
    <li v-for="item in items" :id="item.id">
      {{ item.title }}
      <button @click="deleteItem(item)">X</button>
    </li>
  </ul>
</template>

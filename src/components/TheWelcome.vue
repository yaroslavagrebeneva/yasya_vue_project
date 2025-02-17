<script setup>
import { ref } from 'vue';

// Task#35 - List Manipulations
const items = ref(['Item 1', 'Item 2', 'Item 3']);

const addItem = () => {
  items.value.push(`Item ${items.value.length + 1}`);
};

const removeFirstItem = () => {
  if (items.value.length) items.value.shift();
};

const removeLastItem = () => {
  if (items.value.length) items.value.pop();
};

const removeSecondLastItem = () => {
  if (items.value.length > 1) items.value.splice(-2, 1);
};

const sortItems = () => {
  items.value.sort();
};

const reverseItems = () => {
  items.value.reverse();
};
</script>

<template>
  <div>
    <h1>Task#35 - List Manipulations</h1>
    <ul>
      <li v-for="(item, index) in items" :key="index">
        {{ item }}
      </li>
    </ul>
    <button @click="addItem">Add Item</button>
    <button @click="removeFirstItem">Remove First</button>
    <button @click="removeLastItem">Remove Last</button>
    <button @click="removeSecondLastItem">Remove Second Last</button>
    <button @click="sortItems">Sort Items</button>
    <button @click="reverseItems">Reverse Items</button>
  </div>
</template>

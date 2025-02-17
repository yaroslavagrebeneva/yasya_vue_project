<script setup>
import { ref } from 'vue';

// Task#36 - Styled Component
const items = ref(['Item 1', 'Item 2', 'Item 3']);

const addItem = () => {
  items.value.push(`Item ${items.value.length + 1}`);
};
</script>

<template>
  <div class="styled-container">
    <h1>Task#36 - Styled Component</h1>
    <ul>
      <li v-for="(item, index) in items" :key="index" class="styled-list-item">
        {{ item }}
      </li>
    </ul>
    <button @click="addItem" class="styled-btn">Add Item</button>
  </div>
</template>

<style>
.styled-container {
  text-align: center;
  background-color: #f8f9fa;
  padding: 20px;
  border-radius: 10px;
}

.styled-list-item {
  color: green;
  font-weight: bold;
  margin: 5px 0;
}

.styled-btn {
  margin: 5px;
  padding: 10px;
  border: none;
  background-color: purple;
  color: white;
  cursor: pointer;
  border-radius: 5px;
}

.styled-btn:hover {
  background-color: darkmagenta;
}
</style>

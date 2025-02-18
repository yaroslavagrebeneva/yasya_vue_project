<script setup>
import { ref } from 'vue';

// Task#38 - Object-based Class Binding
const obj = ref({
  done: true,
  selected: false,
});
</script>

<template>
  <div class="styled-container">
    <h1>Task#38 - Object-based Class Binding</h1>
    <p :class="obj">This paragraph has conditional classes.</p>
  </div>
</template>

<style>
.styled-container {
  text-align: center;
  background-color: #f8f9fa;
  padding: 20px;
  border-radius: 10px;
}

.done {
  text-decoration: line-through;
  color: green;
}

.selected {
  font-weight: bold;
  color: red;
}
</style>

<script setup>
import { ref } from 'vue';

// Task#37 - Dynamic Class Binding
const cssClasses = ref('highlight bold');
</script>

<template>
  <div class="styled-container">
    <h1>Task#37 - Dynamic Class Binding</h1>
    <p :class="cssClasses">This is a styled paragraph.</p>
  </div>
</template>

<style>
.styled-container {
  text-align: center;
  background-color: #f8f9fa;
  padding: 20px;
  border-radius: 10px;
}

.highlight {
  color: blue;
}

.bold {
  font-weight: bold;
}
</style>

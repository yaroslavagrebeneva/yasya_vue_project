<script setup>
import { ref } from 'vue';

// Task#40 - Inline Object Class Binding
const obj = ref({
  active: true,
  valid: false,
});
</script>

<template>
  <div class="styled-container">
    <h1>Task#40 - Inline Object Class Binding</h1>
    <p :class="obj">This paragraph has inline class binding.</p>
  </div>
</template>

<style>
.styled-container {
  text-align: center;
  background-color: #f8f9fa;
  padding: 20px;
  border-radius: 10px;
}

.active {
  color: green;
  font-weight: bold;
}

.valid {
  text-decoration: underline;
}
</style>

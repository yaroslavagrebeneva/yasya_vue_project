<script setup>
import { ref } from 'vue';

// Task#41 - Dynamic Class Binding
const isValid = ref(true);
const isDisabled = ref(true);
</script>

<template>
  <div class="styled-container">
    <h1>Task#41 - Dynamic Class Binding</h1>
    <p :class="{ valid: isValid, disabled: isDisabled }">
      This paragraph has dynamic class binding.
    </p>
  </div>
</template>

<style>
.styled-container {
  text-align: center;
  background-color: #f8f9fa;
  padding: 20px;
  border-radius: 10px;
}

.valid {
  color: green;
  font-weight: bold;
}

.disabled {
  opacity: 0.5;
  pointer-events: none;
}
</style>

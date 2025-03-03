<script setup>
import { ref } from 'vue';

// Task#46_1 - Checkbox controlled visibility
const checked = ref(true);
</script>

<template>
  <div class="styled-container">
    <h1>Task#46 - Checkbox Handling</h1>
    
    <!-- Task#46_1: Checkbox controls paragraph visibility -->
    <input type="checkbox" v-model="checked"> Show text
    <p v-if="checked">This text is visible when the checkbox is checked.</p>
  </div>
</template>

<style>
.styled-container {
  text-align: center;
  background-color: #f8f9fa;
  padding: 20px;
  border-radius: 10px;
}

input {
  margin: 10px;
}
</style>

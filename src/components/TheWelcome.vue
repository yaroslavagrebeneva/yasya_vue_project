<script setup>
import { ref } from 'vue';

// Task#43_1 - Two-way binding with input
const message = ref('');

// Task#43_2 - Uppercase transformation
const upperMessage = ref('');

// Task#43_3 - Square of input number
const number = ref(0);
const squaredNumber = ref(0);
</script>

<template>
  <div class="styled-container">
    <h1>Two-way Data Binding</h1>
    
    <!-- Task#43_1: Input binding -->
    <input v-model="message" placeholder="Type something...">
    <p>{{ message }}</p>
    
    <!-- Task#43_2: Uppercase transformation -->
    <input v-model="upperMessage" @input="upperMessage = upperMessage.toUpperCase()" placeholder="Type here (uppercase)">
    <p>{{ upperMessage }}</p>
    
    <!-- Task#43_3: Square of input number -->
    <input v-model.number="number" @input="squaredNumber = number * number" type="number" placeholder="Enter a number">
    <p>Squared: {{ squaredNumber }}</p>
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
  display: block;
  margin: 10px auto;
  padding: 5px;
}
</style>
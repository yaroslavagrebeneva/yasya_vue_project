<script setup>
import { ref } from 'vue';

// Task#44_1 - Square root calculation
const sqrtNumber = ref(0);
const sqrtResult = ref(0);
const calculateSqrt = () => {
  sqrtResult.value = Math.sqrt(sqrtNumber.value);
};

// Task#44_2 - Sum of two numbers
const num1 = ref(0);
const num2 = ref(0);
const sumResult = ref(0);
const calculateSum = () => {
  sumResult.value = num1.value + num2.value;
};

// Task#44_3 - Swap input values
const text1 = ref('');
const text2 = ref('');
const swapTexts = () => {
  [text1.value, text2.value] = [text2.value, text1.value];
};

// Task#44_4 - Split full name
const fullName = ref('');
const surname = ref('');
const name = ref('');
const patronymic = ref('');
const splitName = () => {
  const parts = fullName.value.split(' ');
  surname.value = parts[0] || '';
  name.value = parts[1] || '';
  patronymic.value = parts[2] || '';
};
</script>

<template>
  <div class="styled-container">
    <h1>Task#44 - Form Data Handling</h1>
    
    <!-- Task#44_1: Square root calculation -->
    <input v-model.number="sqrtNumber" type="number" placeholder="Enter a number">
    <button @click="calculateSqrt">Calculate Square Root</button>
    <p>Square Root: {{ sqrtResult }}</p>
    
    <!-- Task#44_2: Sum of two numbers -->
    <input v-model.number="num1" type="number" placeholder="Enter first number">
    <input v-model.number="num2" type="number" placeholder="Enter second number">
    <button @click="calculateSum">Calculate Sum</button>
    <p>Sum: {{ sumResult }}</p>
    
    <!-- Task#44_3: Swap input values -->
    <input v-model="text1" placeholder="First text">
    <input v-model="text2" placeholder="Second text">
    <button @click="swapTexts">Swap Texts</button>
    
    <!-- Task#44_4: Split full name -->
    <input v-model="fullName" placeholder="Enter full name">
    <button @click="splitName">Split Name</button>
    <p>Surname: {{ surname }}</p>
    <p>Name: {{ name }}</p>
    <p>Patronymic: {{ patronymic }}</p>
  </div>
</template>

<style>
.styled-container {
  text-align: center;
  background-color: #f8f9fa;
  padding: 20px;
  border-radius: 10px;
}

input, button {
  display: block;
  margin: 10px auto;
  padding: 5px;
}
</style>

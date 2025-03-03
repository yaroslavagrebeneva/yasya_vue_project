<script setup>
import { ref } from 'vue';

// Task#48_1 & Task#48_2 - Radio button handling
const selectedLanguage = ref('');
const languages = [
  { name: 'English', text: 'Hello, how are you?' },
  { name: 'Spanish', text: 'Hola, ¿cómo estás?' },
  { name: 'French', text: 'Bonjour, comment ça va?' }
];
</script>

<template>
  <div class="styled-container">
    <h1>Task#48 - Radio Button Selection</h1>
    
    <!-- Task#48_1: Radio button group for selecting a native language -->
    <p>Select your native language:</p>
    <div v-for="lang in languages" :key="lang.name">
      <input type="radio" v-model="selectedLanguage" :value="lang.name"> {{ lang.name }}
    </div>
    
    <!-- Task#48_2: Display corresponding phrase based on selection -->
    <p v-if="selectedLanguage">
      {{ languages.find(lang => lang.name === selectedLanguage)?.text }}
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

input {
  margin: 5px;
}
</style>
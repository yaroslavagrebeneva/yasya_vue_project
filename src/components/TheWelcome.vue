<script setup>
import { ref } from 'vue';

// Task#47_1 & Task#47_2 - Checkbox group handling
const selectedLanguages = ref([]);
const languages = ['JavaScript', 'Python', 'Java', 'C++', 'Ruby'];
</script>

<template>
  <div class="styled-container">
    <h1>Task#47 - Checkbox Group</h1>
    
    <!-- Task#47_1: Checkbox group for selecting languages -->
    <p>Select known languages:</p>
    <div v-for="lang in languages" :key="lang">
      <input type="checkbox" v-model="selectedLanguages" :value="lang"> {{ lang }}
    </div>
    
    <!-- Task#47_2: Display selected languages in a list -->
    <ul>
      <li v-for="lang in selectedLanguages" :key="lang">{{ lang }}</li>
    </ul>
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

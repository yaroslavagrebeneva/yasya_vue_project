<script setup>
import { ref } from 'vue';

// Task#45_1 - Live textarea display
const text = ref('');

// Task#45_2 - Convert textarea input to list
const textArea = ref('');
const wordList = ref([]);
const generateList = () => {
  wordList.value = textArea.value.split(' ').filter(word => word);
};
</script>

<template>
  <div class="styled-container">
    <h1>Task#45 - Textarea Handling</h1>
    
    <!-- Task#45_1: Live textarea display -->
    <textarea v-model="text" placeholder="Type something..."></textarea>
    <p>{{ text }}</p>
    
    <!-- Task#45_2: Convert textarea input to list -->
    <textarea v-model="textArea" placeholder="Enter words..."></textarea>
    <button @click="generateList">Generate List</button>
    <ul>
      <li v-for="(word, index) in wordList" :key="index">{{ word }}</li>
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

textarea, button {
  display: block;
  margin: 10px auto;
  padding: 5px;
}
</style>

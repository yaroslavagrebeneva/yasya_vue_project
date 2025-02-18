<script setup>
import { ref } from 'vue';

// Task#39 - Reactive Class Binding
const obj = ref({
  hidden: true,
});

const showElement = () => {
  obj.value.hidden = false;
};

const hideElement = () => {
  obj.value.hidden = true;
};

const toggleElement = () => {
  obj.value.hidden = !obj.value.hidden;
};
</script>

<template>
  <div class="styled-container">
    <h1>Task#39 - Reactive Class Binding</h1>
    <p :class="obj">This paragraph can be shown or hidden.</p>
    <button @click="showElement">Show</button>
    <button @click="hideElement">Hide</button>
    <button @click="toggleElement">Toggle</button>
  </div>
</template>

<style>
.styled-container {
  text-align: center;
  background-color: #f8f9fa;
  padding: 20px;
  border-radius: 10px;
}

.hidden {
  display: none;
}
</style>
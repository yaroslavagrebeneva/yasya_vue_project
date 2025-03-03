<script setup>
import { ref } from 'vue';

// Task#41 - Dynamic Style Binding
const isValid = ref(true);
const isDisabled = ref(true);

// Task#42_1 - Green text, yellow background
const textStyle1 = ref({ color: 'green', backgroundColor: 'yellow' });

// Task#42_2 - Bold and italic text
const textStyle2 = ref({ fontWeight: 'bold', fontStyle: 'italic' });
</script>

<template>
  <div class="styled-container">
    <h1>Task#41 - Dynamic Style Binding</h1>
    <p :class="{ valid: isValid, disabled: isDisabled }" 
       :style="textStyle1">
      This paragraph has green text and yellow background.
    </p>
    <p :style="textStyle2">
      This paragraph has bold and italic text.
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

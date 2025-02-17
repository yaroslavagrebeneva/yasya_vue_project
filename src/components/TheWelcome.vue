<script setup>
import { ref } from 'vue';
</script>

<template>
  <div>
    <h1>Task#32 - Numbered Paragraphs</h1>
    <p v-for="num in 30" :key="num">
      {{ num }}
    </p>
  </div>
</template>

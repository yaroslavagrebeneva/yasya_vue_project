<script setup>
import { ref } from 'vue';

// Task#33 - Filtering Positive Numbers
const items = ref([1, -2, 3, -4, 5]);
</script>

<template>
  <div>
    <h1>Task#33 - Positive Numbers</h1>
    <ul>
      <template v-for="item in items">
        <li v-if="item > 0" :key="item">
          {{ item }}
        </li>
      </template>
    </ul>
  </div>
</template>

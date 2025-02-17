<script setup>
import { ref } from 'vue';

// Task#34 - Displaying Products with Unique Keys
const products = ref([
  { id: 1, name: 'product1' },
  { id: 2, name: 'product2' },
  { id: 3, name: 'product3' },
]);
</script>

<template>
  <div>
    <h1>Task#34 - Product List</h1>
    <ul>
      <li v-for="product in products" :key="product.id">
        {{ product.name }}
      </li>
    </ul>
  </div>
</template>

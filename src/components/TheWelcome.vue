<script setup>
import { ref } from 'vue';

// Task#27 - Перебор массива и вывод элементов в div
const items = ref([1, 2, 3, 4, 5]);

// Task#28 - Вывод ключей массива в списке ul
const arr = ref(['x', 'y', 'z']);
</script>

<template>
  <div>
    <h1>Task#27</h1>
    <div v-for="item in items" :key="item">{{ item }}</div>

    <h1>Task#28</h1>
    <ul>
      <li v-for="(elem, key) in arr" :key="key">{{ key }}</li>
    </ul>
  </div>
</template>

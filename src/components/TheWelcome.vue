<script setup>
import { ref } from 'vue';

// Task#29 - Перебор объекта и вывод ключей, значений и индексов
const users = ref({
  user1: '100$',
  user2: '200$',
  user3: '300$'
});
</script>

<template>
  <div>
    <h1>Task#29</h1>
    <ul>
      <li v-for="(value, key, index) in users" :key="key">
        {{ key }} - {{ value }} - {{ index + 1 }}
      </li>
    </ul>
  </div>
</template>

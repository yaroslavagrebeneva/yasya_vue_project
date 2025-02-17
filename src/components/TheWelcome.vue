<script setup>
import { ref } from 'vue';

// Новое задание - использование v-else
const isAdmin = ref(true);
</script>

<template>
  <div>
    <h1>Task#22</h1>
    <p v-if="isAdmin">Вы администратор</p>
    <p v-else>Вы не администратор</p>
  </div>
</template>

<script setup>
import { ref } from 'vue';

// Task#26 - скрытие группы абзацев
const isVisible = ref(true);
const toggleVisibility = () => {
  isVisible.value = !isVisible.value;
};
</script>

<template>
  <div>
    <h1>Task#26</h1>
    <button @click="toggleVisibility">{{ isVisible ? 'Скрыть' : 'Показать' }} абзацы</button>
    <template v-if="isVisible">
      <p>Абзац 1</p>
      <p>Абзац 2</p>
      <p>Абзац 3</p>
    </template>
  </div>
</template>

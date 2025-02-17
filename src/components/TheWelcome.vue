<script setup>
import { ref } from 'vue';

// Task#27 - тоггл абзаца с v-show
const isParagraphVisible = ref(true);
const toggleParagraph = () => {
  isParagraphVisible.value = !isParagraphVisible.value;
};
</script>

<template>
  <div>
    <h1>Task#27</h1>
    <button @click="toggleParagraph">{{ isParagraphVisible ? 'Скрыть' : 'Показать' }} абзац</button>
    <p v-show="isParagraphVisible">Этот абзац можно скрыть или показать</p>
  </div>
</template>

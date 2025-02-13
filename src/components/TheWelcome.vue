<script setup>
import { ref } from 'vue';

const visible = ref(true);

// Функция для предотвращения перехода по ссылке
const preventNavigation = (event) => {
  event.preventDefault();
};

// Функция для обработки клика по кнопке (только первый клик)
const clicked = ref(false);
const handleClickOnce = () => {
  if (!clicked.value) {
    clicked.value = true;
    console.log('Кнопка нажата один раз');
  }
};
</script>

<template>
  <div>
    <h1>Task#16</h1>
    <a href="https://example.com" @click.prevent="preventNavigation">Запрещенная ссылка</a>
    <br />
    <button @click.once="handleClickOnce">Кликни один раз</button>
    <br />
    <h1>Task#17</h1>
    <p v-if="visible">Этот абзац виден, если visible = true</p>
    <p v-if="!visible">Этот абзац виден, если visible = false</p>
  </div>
</template>

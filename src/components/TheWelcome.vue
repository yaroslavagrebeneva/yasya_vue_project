<script setup>
import { ref } from 'vue';

// Task#18 - Инвертируем условие
const hidden = ref(false);

// Task#19 - Показ и скрытие абзаца
const isParagraphVisible = ref(false);
const showParagraph = () => { isParagraphVisible.value = true; };
const hideParagraph = () => { isParagraphVisible.value = false; };

// Task#20 - Тоггл для каждого абзаца
const para1 = ref(false);
const para2 = ref(false);
const para3 = ref(false);

// Task#21 - Тоггл с изменением текста кнопки
const paraState = ref([false, false, false]);
const toggleParagraph = (index) => {
  paraState.value[index] = !paraState.value[index];
};
</script>

<template>
  <div>
    <h1>Task#18</h1>
    <p v-if="!hidden">text</p>
    
    <h1>Task#19</h1>
    <button @click="showParagraph">Показать абзац</button>
    <button @click="hideParagraph">Скрыть абзац</button>
    <p v-if="isParagraphVisible">Этот абзац можно показать и скрыть</p>
    
    <h1>Task#20</h1>
    <button @click="() => para1 = !para1">Toggle 1</button>
    <p v-if="para1">Абзац 1</p>
    <button @click="() => para2 = !para2">Toggle 2</button>
    <p v-if="para2">Абзац 2</p>
    <button @click="() => para3 = !para3">Toggle 3</button>
    <p v-if="para3">Абзац 3</p>
    
    <h1>Task#21</h1>
    <button @click="() => toggleParagraph(0)">{{ paraState[0] ? 'Скрыть' : 'Показать' }} абзац 1</button>
    <p v-if="paraState[0]">Абзац 1</p>
    <button @click="() => toggleParagraph(1)">{{ paraState[1] ? 'Скрыть' : 'Показать' }} абзац 2</button>
    <p v-if="paraState[1]">Абзац 2</p>
    <button @click="() => toggleParagraph(2)">{{ paraState[2] ? 'Скрыть' : 'Показать' }} абзац 3</button>
    <p v-if="paraState[2]">Абзац 3</p>
  </div>
</template>

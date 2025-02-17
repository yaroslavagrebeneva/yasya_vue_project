<script setup>
import { ref } from 'vue';

// Task#23 - отображение дня недели
const day = ref('Понедельник'); // Здесь можно менять день недели

// Task#24 - отображение возраста
const age = ref(25);
</script>

<template>
  <div>
    <h1>Task#23</h1>
    <p v-if="day === 'Понедельник'">Понедельник</p>
    <p v-else-if="day === 'Вторник'">Вторник</p>
    <p v-else-if="day === 'Среда'">Среда</p>
    <p v-else-if="day === 'Четверг'">Четверг</p>
    <p v-else-if="day === 'Пятница'">Пятница</p>
    <p v-else-if="day === 'Суббота'">Суббота</p>
    <p v-else-if="day === 'Воскресенье'">Воскресенье</p>

    <h1>Task#24</h1>
    <p v-if="age < 18">Подросток</p>
    <p v-else-if="age >= 19 && age <= 25">Молодой человек</p>
    <p v-else>Мужчина</p>
  </div>
</template>
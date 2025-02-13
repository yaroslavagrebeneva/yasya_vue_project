<script setup>
import { ref, computed } from 'vue';

const cost = ref(100); // Цена продукта
const amount = ref(2); // Количество продуктов

// Вычисляемое свойство для полной стоимости
const price = computed(() => cost.value * amount.value);

// Функция для изменения цены
const changeCost = () => {
  cost.value += 50;
};
</script>

<template>
  <div>
    <h1>Task#15</h1>
    <p>Цена: {{ cost }}</p>
    <p>Количество: {{ amount }}</p>
    <p>Полная стоимость: {{ price }}</p>
    <button @click="changeCost">Изменить цену</button>
  </div>
</template>

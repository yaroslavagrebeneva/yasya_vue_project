<template>
  <div>
    <!-- Задание 1 -->
    <label for="day">Выберите день недели:</label>
    <select v-model="selectedDay" id="day">
      <option value="Monday">Понедельник</option>
      <option value="Tuesday">Вторник</option>
      <option value="Wednesday">Среда</option>
      <option value="Thursday">Четверг</option>
      <option value="Friday">Пятница</option>
      <option value="Saturday">Суббота</option>
      <option value="Sunday">Воскресенье</option>
    </select>
    <p>Вы выбрали: {{ selectedDay }}</p>

    <!-- Задание 2 -->
    <label for="daySelect">Выберите день:</label>
    <select v-model="selectedDay" id="daySelect">
      <option v-for="n in 31" :key="n" :value="n">{{ n }}</option>
    </select>

    <label for="monthSelect">Выберите месяц:</label>
    <select v-model="selectedMonth" id="monthSelect">
      <option v-for="n in 12" :key="n" :value="n">{{ n }}</option>
    </select>

    <label for="yearSelect">Выберите год:</label>
    <select v-model="selectedYear" id="yearSelect">
      <option v-for="n in 100" :key="n" :value="2000 + n">{{ 2000 + n }}</option>
    </select>

    <p>Дата: {{ selectedDay }}-{{ selectedMonth }}-{{ selectedYear }}</p>

    <!-- Задание 3 -->
    <label for="daySelect">Выберите день:</label>
    <select v-model="selectedDay" id="daySelect">
      <option v-for="n in 31" :key="n" :value="n">{{ n }}</option>
    </select>

    <label for="monthSelect">Выберите месяц:</label>
    <select v-model="selectedMonth" id="monthSelect">
      <option v-for="n in 12" :key="n" :value="n">{{ n }}</option>
    </select>

    <label for="yearSelect">Выберите год:</label>
    <select v-model="selectedYear" id="yearSelect">
      <option v-for="n in 100" :key="n" :value="2000 + n">{{ 2000 + n }}</option>
    </select>

    <p>Дата: {{ selectedDay }}-{{ selectedMonth }}-{{ selectedYear }}</p>
  </div>
</template>

<script>
export default {
  data() {
    const currentDate = new Date();
    return {
      selectedDay: currentDate.getDate(),
      selectedMonth: currentDate.getMonth() + 1, // months are 0-indexed
      selectedYear: currentDate.getFullYear(),
      selectedDayWeek: currentDate.toLocaleString('default', { weekday: 'long' }),
    };
  },
};
</script>
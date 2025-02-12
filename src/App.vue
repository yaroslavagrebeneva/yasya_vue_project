<script setup>
import { ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue';
import TheWelcome from './components/TheWelcome.vue';

// Task#12_1: Вспомогательный метод для получения дня недели
const getWeekday = (num) => {
  const weekdays = ['Воскресенье', 'Понедельник', 'Вторник', 'Среда', 'Четверг', 'Пятница', 'Суббота'];
  return weekdays[num] || 'Некорректное число';
};

// Task#12_2: Основной метод для вывода текущего дня недели
const showCurrentWeekday = () => {
  const today = new Date().getDay(); // Получаем номер дня недели (0-6)
  alert(getWeekday(today));
};
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
    <TheWelcome />

    <!-- Task#12_1 -->
    <section>
      <h2>Task#12_1</h2>
      <p>Пример: 3 -> {{ getWeekday(3) }}</p>
      <p>Пример: 6 -> {{ getWeekday(6) }}</p>
    </section>

    <!-- Task#12_2 -->
    <section>
      <h2>Task#12_2</h2>
      <button @click="showCurrentWeekday">Показать текущий день недели</button>
    </section>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}

section {
  margin: 20px 0;
}

button {
  padding: 10px 15px;
  font-size: 16px;
  cursor: pointer;
  background-color: #42b983;
  color: white;
  border: none;
  border-radius: 5px;
  transition: background 0.3s;
}

button:hover {
  background-color: #369f75;
}
</style>

<script setup>
import { ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue';
import TheWelcome from './components/TheWelcome.vue';

// Task#14_1: Реактивное свойство text
const text = ref('Начальный текст');

// Task#14_2: Функция для изменения текста
const changeText = () => {
  text.value = 'Новое значение!';
};

// Task#14_3: Функции для установки разных значений
const setFirstText = () => {
  text.value = 'Первый текст';
};

const setSecondText = () => {
  text.value = 'Второй текст';
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

    <!-- Task#14_1 -->
    <section>
      <h2>Task#14_1</h2>
      <p>{{ text }}</p>
    </section>

    <!-- Task#14_2 -->
    <section>
      <h2>Task#14_2</h2>
      <p>{{ text }}</p>
      <button @click="changeText">Изменить текст</button>
    </section>

    <!-- Task#14_3 -->
    <section>
      <h2>Task#14_3</h2>
      <p>{{ text }}</p>
      <button @click="setFirstText">Первый вариант</button>
      <button @click="setSecondText">Второй вариант</button>
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
  margin-right: 10px;
}

button:hover {
  background-color: #369f75;
}
</style>

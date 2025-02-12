<script setup>
import { ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue';
import TheWelcome from './components/TheWelcome.vue';

// Task#10_1 и Task#10_2: Метод для вывода текущей даты
const showDate = () => {
  alert(new Date().toLocaleDateString());
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

    <!-- Task#10_1 -->
    <section>
      <h2>Task#10_1</h2>
      <button @click="showDate">Показать дату (клик)</button>
    </section>

    <!-- Task#10_2 -->
    <section>
      <h2>Task#10_2</h2>
      <button @mouseover="showDate">Показать дату (наведение)</button>
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

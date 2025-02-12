<script setup>
import HelloWorld from './components/HelloWorld.vue';
import TheWelcome from './components/TheWelcome.vue';

// Task#13_1: Метод для вывода квадрата числа
const showSquare = (num) => {
  alert(`Квадрат числа ${num}: ${num * num}`);
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

    <!-- Task#13_1 и Task#13_2 -->
    <section>
      <h2>Task#13_1</h2>
      <p>Нажмите кнопку, чтобы увидеть квадрат числа:</p>
      <button @click="showSquare(2)">Квадрат 2</button>
      <button @click="showSquare(3)">Квадрат 3</button>
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

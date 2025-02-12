<script setup>
import { ref, computed } from 'vue';
import HelloWorld from './components/HelloWorld.vue';
import TheWelcome from './components/TheWelcome.vue';

// Task#8_1: Вывести сумму значений объекта
const obj = ref({ x: 1, y: 2, z: 3 });
const sumObj = computed(() => Object.values(obj.value).reduce((sum, num) => sum + num, 0));
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

    <!-- Task#8_1 -->
    <section>
      <h2>Task#8_1</h2>
      <p>Сумма элементов объекта: <strong>{{ sumObj }}</strong></p>
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
</style>

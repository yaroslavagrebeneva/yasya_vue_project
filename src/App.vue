<script setup>
import { ref, computed } from 'vue';
import HelloWorld from './components/HelloWorld.vue';
import TheWelcome from './components/TheWelcome.vue';

// Task#7_1: Вывести каждый элемент массива в отдельном абзаце
const arr1 = ref(['x', 'y', 'z']);

// Task#7_2: Вывести сумму элементов массива
const arr2 = ref([1, 2, 3]);
const sumArr2 = computed(() => arr2.value.reduce((sum, num) => sum + num, 0));
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

    <section>
      <h1>Task#7_1</h1>
      <h3 v-for="(item, index) in arr1" :key="index">{{ item }}</h3>
    </section>

    <section>
      <h1>Task#7_2</h1>
      <h3>Сумма элементов массива: <strong>{{ sumArr2 }}</strong></h3>
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

<script setup>
import { ref, computed } from 'vue';
import HelloWorld from './components/HelloWorld.vue';
import TheWelcome from './components/TheWelcome.vue';

// Task#6_1: Вывести квадрат свойства num
const num = ref(5);
const squaredNum = computed(() => num.value ** 2);

// Task#6_2: Вывести сумму num1, num2, num3
const num1 = ref(1);
const num2 = ref(2);
const num3 = ref(3);
const sumNums = computed(() => num1.value + num2.value + num3.value);
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
      <h2>Task#6_1</h2>
      <p>Квадрат числа {{ num }}: <strong>{{ squaredNum }}</strong></p>
    </section>

    <section>
      <h2>Task#6_2</h2>
      <p>Сумма чисел {{ num1 }}, {{ num2 }}, {{ num3 }}: <strong>{{ sumNums }}</strong></p>
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

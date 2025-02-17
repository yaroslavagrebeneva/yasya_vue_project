<script setup>
import { ref } from 'vue';

// Task#31_1 - Перебор массива объектов и вывод пользователей
const users = ref([
  { name: 'name1', surn: 'surn1' },
  { name: 'name2', surn: 'surn2' },
  { name: 'name3', surn: 'surn3' },
]);

// Task#31_2 - Перебор массива ссылок и формирование списка
const hrefs = ref([
  { href: '1.html', text: 'text1' },
  { href: '2.html', text: 'text2' },
  { href: '3.html', text: 'text3' },
]);

// Task#31_3 - Перебор массива продуктов и формирование таблицы
const products = ref([
  { name: 'product1', price: 100, quantity: 5 },
  { name: 'product2', price: 200, quantity: 4 },
  { name: 'product3', price: 300, quantity: 3 },
]);
</script>

<template>
  <div>
    <h1>Task#31_1 - Users List</h1>
    <p v-for="user in users" :key="user.name">
      {{ user.name }} {{ user.surn }}
    </p>

    <h1>Task#31_2 - Links List</h1>
    <ul>
      <li v-for="link in hrefs" :key="link.href">
        <a :href="link.href">{{ link.text }}</a>
      </li>
    </ul>

    <h1>Task#31_3 - Products Table</h1>
    <table border="1">
      <tr v-for="product in products" :key="product.name">
        <td>{{ product.name }}</td>
        <td>{{ product.price }}</td>
        <td>{{ product.quantity }}</td>
      </tr>
    </table>
  </div>
</template>

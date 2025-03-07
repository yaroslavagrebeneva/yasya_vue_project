<template>
  <div>
    <!-- Задание 1 -->
    <input v-model="newItem" type="text" />
    <button @click="addItemToEnd">Add to end</button>
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>

    <!-- Задание 2 -->
    <button @click="addItemToStart">Add to start</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newItem: '',
      items: ['item 1', 'item 2', 'item 3'],
    };
  },
  methods: {
    addItemToEnd() {
      if (this.newItem.trim() !== '') {
        this.items.push(this.newItem);
        this.newItem = '';
      }
    },
    addItemToStart() {
      if (this.newItem.trim() !== '') {
        this.items.unshift(this.newItem);
        this.newItem = '';
      }
    },
  },
};
</script>
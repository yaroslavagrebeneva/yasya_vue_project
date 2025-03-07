<template>
  <div>
    <ul>
      <li v-for="(item, index) in items" :key="index" @click="removeItem(index)">
        {{ item }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: ['item 1', 'item 2', 'item 3', 'item 4'],
    };
  },
  methods: {
    removeItem(index) {
      this.items.splice(index, 1);
    },
  },
};
</script>
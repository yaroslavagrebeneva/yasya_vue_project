<template>
  <div>
    <!-- Задание 1 -->
    <input type="text" v-bind:disabled="isDisabled" id="inputField" />
    <button @click="toggleInput">Toggle Input</button>

    <!-- Задание 2 -->
    <label for="checkbox">Enable input:</label>
    <input type="checkbox" v-model="isEnabled" id="checkbox" />
    <input type="text" :disabled="!isEnabled" id="inputField" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      isDisabled: false,
      isEnabled: true,
    };
  },
  methods: {
    toggleInput() {
      this.isDisabled = !this.isDisabled;
    },
  },
};
</script>
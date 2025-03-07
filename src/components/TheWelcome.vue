<template>
  <div>
    <label for="city">В каком городе вы живете?</label>
    <select v-model="city" id="city">
      <option value="Moscow">Москва</option>
      <option value="Saint Petersburg">Санкт-Петербург</option>
      <option value="Novosibirsk">Новосибирск</option>
      <option value="Yekaterinburg">Екатеринбург</option>
      <option value="Kazan">Казань</option>
    </select>

    <p>Вы живете в: {{ city }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      city: '',
    };
  },
};
</script>
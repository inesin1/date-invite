<script setup lang="ts">
import { ref } from 'vue';

const page = ref(1)
const nextPage = () => {
  page.value = page.value + 1
}
</script>

<template>
  <div class="container">
    <div v-if="page == 1">
        <h1>Пойдем сегодня на свидание?</h1>
      <div class="button-box">
        <button @click="nextPage">Да</button>
        <button @click="nextPage">Конечно да</button>
      </div>
    </div>

    <div v-if="page == 2">
      <h1>Супер!)</h1>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
}
.button-box {
  display: flex;
  flex-direction: row;
  gap: 16px;
}
</style>

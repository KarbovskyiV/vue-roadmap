<template>
  <h1>{{ header }}</h1>
  <ul>
    <li v-for="{ id, label } in items" :key="id"> {{ label }}</li>
  </ul>
</template>

<script setup>
import { ref } from 'vue';

const header = ref('Shopping List App');
const items = ref({
  1: { id: 1, label: '10 party hats' },
  2: { id: 2, label: '2 board games' },
  3: { id: 3, label: '20 cups' },
});
</script>

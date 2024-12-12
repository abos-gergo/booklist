<script setup lang="ts">
import CardView from './pages/CardPage.vue'
import TableView from './pages/TablePage.vue'
import Header from './components/Header.vue'
import { ref } from 'vue';

const cardView = ref(false);
</script>

<template>
  <Header v-model="cardView"></Header>

  <main>
    <CardView v-if="cardView"></CardView>
    <TableView v-else></TableView>
  </main>
</template>

<style scoped></style>

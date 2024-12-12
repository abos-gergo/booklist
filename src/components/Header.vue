<script setup lang="ts">
const cardView = defineModel<boolean>();

defineProps<{
  cardView: boolean
}>()

const toggleView = () => {
  cardView.value = !cardView.value
}
</script>

<template>
  <header class="header">
    <h1 class="header-title">Booklist</h1>
    <button @click="toggleView" class="toggle-btn">
      {{ cardView ? 'Switch to Table View' : 'Switch to Card View' }}
    </button>
  </header>
</template>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 30px;
  background-color: #4caf50;
  color: white;
}

.header-title {
  font-size: 24px;
  font-weight: bold;
  margin: 0;
}

.toggle-btn {
  padding: 8px 16px;
  font-size: 16px;
  cursor: pointer;
  background-color: #fff;
  color: #4caf50;
  border: none;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

.toggle-btn:hover {
  background-color: #45a049;
  color: #fff;
}
</style>

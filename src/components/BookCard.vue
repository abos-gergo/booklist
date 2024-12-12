<!-- BookCard.vue -->
<script setup lang="ts">
defineProps<{
  title: string
  author: string
  img_url: string
}>()
</script>

<template>
  <div class="card">
    <img :src="img_url" alt="Book cover" class="card-img" />
    <div class="card-content">
      <h5 class="card-title">{{ title }}</h5>
      <h6 class="card-author">{{ author }}</h6>
    </div>
  </div>
</template>

<style scoped>
.card {
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  max-width: 200px;
  margin: 10px;
  transition:
    transform 0.3s ease,
    box-shadow 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);
}

.card-img {
  width: 100%;
  height: 250px;
  object-fit: cover;
  border-bottom: 2px solid #f1f1f1;
}

.card-content {
  padding: 15px;
}

.card-title {
  font-size: 18px;
  font-weight: bold;
  margin: 0;
  color: #333;
}

.card-author {
  font-size: 14px;
  color: #555;
  margin-top: 5px;
}
</style>

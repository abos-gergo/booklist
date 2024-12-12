<script setup lang="ts">
import BookCard from './../components/BookCard.vue'
import books from '../bookdata.ts'
</script>

<template>
  <div class="card-container">
    <BookCard
      v-for="(book, index) in books"
      :key="index"
      :title="book.title"
      :author="book.author"
      :img_url="book.img_url"
    />
  </div>
</template>

<style scoped>
.card-container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
}
</style>

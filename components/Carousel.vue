<template>
  <carousel-3d
    :controls-visible="true"
    :clickable="true"
    :width="500"
    :height="600"
    :perspective="0"
  >
    <slide v-for="(book, index) in books" :key="index" :index="index">
      <NuxtLink :to="{ path: `${book.category}/${book.slug}` }">
        <Book :book="book" />
      </NuxtLink>
    </slide>
  </carousel-3d>
</template>

<script>
import { Carousel3d, Slide } from 'vue-carousel-3d'
import { books } from '../store'

export default {
  components: {
    Carousel3d,
    Slide,
  },
  data: () => {
    return {
      books,
    }
  },
}
</script>

<style>
.carousel-3d-container .carousel-3d-slide {
  background-color: transparent;
  border: none;
}
</style>

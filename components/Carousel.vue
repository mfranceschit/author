<template>
  <client-only>
    <carousel-3d
      v-if="window.width >= 550"
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
    <carousel-3d
      v-else
      :disable3d="true"
      :controls-visible="true"
      :clickable="true"
      :width="100"
      :space="105"
      :height="600"
      :perspective="0"
    >
      <slide v-for="(book, index) in books" :key="index" :index="index">
        <NuxtLink :to="{ path: `${book.category}/${book.slug}` }">
          <BookSpine :book="book" />
        </NuxtLink>
      </slide>
    </carousel-3d>
  </client-only>
</template>

<script>
import { books } from '../store'

export default {
  data: () => {
    return {
      books,
      window: {
        width: 0,
        height: 0,
      },
    }
  },
  created() {
    // eslint-disable-next-line nuxt/no-globals-in-created
    window.addEventListener('resize', this.handleResize)
    this.handleResize()
  },
  destroyed() {
    window.removeEventListener('resize', this.handleResize)
  },
  methods: {
    handleResize() {
      this.window.width = window.innerWidth
      this.window.height = window.innerHeight
    },
  },
}
</script>

<style>
.carousel-3d-container .carousel-3d-slide {
  background-color: transparent;
  border: none;
}
</style>

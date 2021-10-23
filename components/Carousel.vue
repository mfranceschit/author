<template>
  <carousel-3d
    :controls-visible="true"
    :clickable="true"
    :width="500"
    :height="600"
    :perspective="0"
  >
    <slide :index="0">
      <NuxtLink to="/read/the-boy-must-die">
        <Book />
      </NuxtLink>
    </slide>
    <slide :index="1"><Book /> </slide>
    <slide :index="2"> <Book /> </slide>
  </carousel-3d>
</template>

<script>
import { Carousel3d, Slide } from 'vue-carousel-3d'

export default {
  components: {
    Carousel3d,
    Slide,
  },
}
</script>

<style>
.carousel-3d-container .carousel-3d-slide {
  background-color: transparent;
  border: none;
}
</style>

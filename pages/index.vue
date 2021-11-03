<template>
  <main class="layout">
    <h1>Marco's Writings</h1>
    <Carousel />
  </main>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style>
@font-face {
  font-family: 'Parisienne';
  src: url('../assets/fonts/Parisienne/Parisienne-Regular.ttf');
}

.layout {
  display: flex;
  height: 100vh;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

body {
  background: url('~assets/images/white_wall.png');
}

.layout h1 {
  font-family: 'Parisienne';
  font-size: 48px;
}
</style>

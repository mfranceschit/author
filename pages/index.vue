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
.layout {
  display: flex;
  height: 100vh;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.html,
body {
  background-color: #c4bec6;
  display: border-box;
}
</style>

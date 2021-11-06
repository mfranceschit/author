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

@font-face {
  font-family: 'ZenOldMinchoRegular';
  src: url('../assets/fonts/Zen_Old_Mincho/ZenOldMincho-Regular.ttf');
}

@font-face {
  font-family: 'ZenOldMinchoBlack';
  src: url('../assets/fonts/Zen_Old_Mincho/ZenOldMincho-Black.ttf');
}

@font-face {
  font-family: 'ZenOldMinchoBlackBold';
  src: url('../assets/fonts/Zen_Old_Mincho/ZenOldMincho-Bold.ttf');
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
  font-size: 4em;
}

@media screen and (max-width: 768px) {
  .layout h1 {
    display: none;
  }
}
</style>

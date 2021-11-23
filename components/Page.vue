<template>
  <article
    class="page"
    :class="[article.category === 'stories' ? 'story' : 'thought']"
  >
    <h1>{{ article.title }}</h1>
    <figure>
      <img
        v-if="article.img"
        class="cover-image"
        :src="require(`~/assets/images/${article.img}`)"
        :alt="article.alt"
      />
    </figure>
    <nuxt-content :document="article" />
  </article>
</template>

<script>
export default {
  props: {
    article: {
      title: String,
      img: String,
      alt: String,
      category: String,
    },
  },
}
</script>

<style>
body {
  background: url('~assets/images/white_wall.png');
}

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

.cover-image {
  width: 100%;
}

.nuxt-content h2 {
  font-weight: bold;
  font-family: 'Parisienne';

  font-size: 28px;
}
.nuxt-content h3 {
  font-weight: bold;
  font-family: 'Parisienne';

  font-size: 22px;
}
.nuxt-content p {
  font-family: 'ZenOldMinchoRegular';
  margin-bottom: 20px;
}

.nuxt-content > blockquote {
  padding: 5em 0;
}

.nuxt-content > blockquote > p:first-child {
  text-align: left;
}

.nuxt-content > blockquote > p {
  font-family: 'Parisienne';
  font-size: 1.5em;
  text-align: center;
}

.page.story .nuxt-content > p:first-of-type::first-letter {
  font-family: 'Parisienne';
  font-size: 2em;
}

.page.story .nuxt-content > p:last-child {
  text-align: center;
  font-family: 'Parisienne';
  font-size: 2em;
  font-weight: bold;
}

.page-container {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  margin-top: 1em;
}

.page {
  background-color: white;
  max-width: 600px;
  min-height: 850px;
  margin: 1em;
  padding: 1em 2em;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  font-family: 'Helvetica';
}

.page h1 {
  text-align: center;
  font-size: 3em;
  font-family: 'Parisienne';
}

.page figure {
  margin: 0 0 1rem;
}
</style>

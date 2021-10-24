<template>
  <article class="page">
    <h1>{{ article.title }}</h1>
    <figure>
      <img class="cover-image" :src="article.img" :alt="article.alt" />
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
    },
  },
}
</script>

<style>
.cover-image {
  width: 100%;
}

.nuxt-content h2 {
  font-weight: bold;
  font-size: 28px;
}
.nuxt-content h3 {
  font-weight: bold;
  font-size: 22px;
}
.nuxt-content p {
  margin-bottom: 20px;
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
  padding: 1em;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  font-family: 'Helvetica';
}

.page h1 {
  text-align: center;
}
</style>

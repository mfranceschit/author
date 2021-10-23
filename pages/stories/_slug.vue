<template>
  <main class="page-container">
    <article class="page">
      <h1>{{ article.title }}</h1>
      <p>{{ article.description }}</p>
      <img :src="article.img" :alt="article.alt" />
      <p>Article last updated: {{ formatDate(article.updatedAt) }}</p>

      <nuxt-content :document="article" />
    </article>
  </main>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const article = await $content('stories', params.slug).fetch()

    return { article }
  },
  methods: {
    formatDate(date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    },
  },
}
</script>

<style>
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
}

.page {
  background-color: white;
  width: 600px;
  margin: 1em;
  padding: 1em;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}
</style>

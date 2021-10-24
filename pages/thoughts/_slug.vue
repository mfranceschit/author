<template>
  <main class="page-container">
    <HomeIcon />
    <Page :article="article" />
  </main>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const article = await $content('thoughts', params.slug).fetch()

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

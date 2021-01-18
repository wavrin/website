<template>
  <article>
    <div class="p-2">
      <NuxtLink to="/">
        <font-awesome-icon :icon="['fas', 'chevron-circle-left']"/>
      </NuxtLink>
    </div>
    <p class="text-gray-500">
      {{ article.timestamp }}
    </p>
    <nuxt-content :document="article" />
  </article>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const article = await $content('articles', params.slug).fetch()

    return { article }
  },
  methods: {
    formatDate (date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    }
  }
}
</script>
<style>
.nuxt-content p {
  margin-bottom: 20px;
}

.nuxt-content a {
  color: blue;
}
</style>

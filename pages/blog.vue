<template>
  <section class="page-banner">
    <div class="container">
        <h1 class="page-banner__title">
          {{pageInfo.title.rendered}}
        </h1>
    </div>
  </section>
</template>

<script>
  export default {
    async asyncData({ app }) {
      let { data } = await app.$axios.get('https://creafresh.markupus.tech/wp-json/wp/v2/pages/72/?_embed');
      return {
        pageInfo: data
      }
    },
    head() {
      return {
        title: this.pageInfo.title.rendered
      }
    },
  }
</script>

<style>

</style>

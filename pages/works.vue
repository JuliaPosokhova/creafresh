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
    let { data } = await app.$axios.get(
      "https://creafresh.markupus.tech/wp-json/wp/v2/pages/70/?_embed"
    );
    return {
      pageInfo: data
    };
  },
  head() {
    return {
      title: this.pageInfo.title.rendered
    };
  }
};
</script>

<style lang="scss">
.page-banner {
  min-height: 60vh;
  padding-top: 75px;
  display: flex;
  align-items: center;
  @include desktop-s {
    padding-top: 100px;
    min-height: 75vh;
  }
}

.page-banner__title {
  font-weight: 700;
  font-size: 30px;
  line-height: 36px;
  margin-bottom: 32px;
  @include tablet {
    font-size: 50px;
    line-height: 60px;
    margin-bottom: 0;
  }
  @include desktop-s {
    font-weight: 900;
  }
  @include desktop-m {
    font-size: 72px;
    line-height: 82px;
  }
}
</style>

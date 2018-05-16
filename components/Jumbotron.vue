<template>
  <section class="jumbotron">
    <div class="container">
      <div v-html="jumbotron.text" class="jumbotron__content"></div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      jumbotron: [],
      errors: []
    };
  },
  created() {
    this.$axios
      .$get("https://creafresh.markupus.tech/wp-json/wp/v2/pages/23/?_embed")
      .then(response => {
        this.jumbotron = response.acf.modules[2].content;
      })
      .catch(e => {
        this.errors.push(e);
      });
  }
};
</script>


<style lang="scss">
.jumbotron {
  padding-top: 17px;
  padding-bottom: 20px;
  @include tablet {
    padding-top: 86px;
    padding-bottom: 60px;
  }
  p {
    font-size: 18px;
    line-height: 30px;
    font-weight: 500;
    margin-bottom: 30px;
    @include tablet {
      font-size: 20px;
      line-height: 36px;
      margin-bottom: 36px;
    }
  }
  .button {
    margin-top: 10px;
    letter-spacing: 1px;
  }
}

.jumbotron__content {
  @include desktop-m {
    max-width: 780px;
    margin: 0 auto;
  }
}
</style>

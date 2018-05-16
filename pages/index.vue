<template>
  <div class="content">
    <banner/>
    <works/>
    <jumbotron/>
    <feeds get="user" resolution="standard_resolution" sort-by="most-recent" v-bind:limit="5" v-bind:links="false"></feeds>
  </div>
</template>


<script>
import Banner from "@/components/Banner.vue";
import Works from "@/components/Works.vue";
import Jumbotron from "@/components/Jumbotron.vue";
import Feeds from "@/components/Feeds.vue";

export default {
  async asyncData({ app }) {
    let { data } = await app.$axios.get(
      "https://creafresh.markupus.tech/wp-json/wp/v2/pages/23/?_embed"
    );
    return {
      pageInfo: data
    };
  },

  head() {
    return {
      title: this.pageInfo.title.rendered
    };
  },
  components: {
    Banner,
    Works,
    Jumbotron,
    Feeds
  }
};
</script>

<style>
</style>

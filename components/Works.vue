<template>
  <section class="works">
    <div class="container">
      <div class="works__list">
        <div
          class="works__item"
          :class="{'works__item--small': (work['_embedded']['wp:featuredmedia'][0].media_details.width < 700)}"
          v-for="(work, index) in works" :key="index">
          <a
          :href="work.link" class="works__link">
            <progressive-img
              :src="work['_embedded']['wp:featuredmedia'][0].source_url"
              :placeholder="work['_embedded']['wp:featuredmedia'][0].media_details.sizes.medium.source_url">
            </progressive-img>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      works: [],
      errors: []
    };
  },
  created() {
    this.$axios
      .$get("https://creafresh.markupus.tech/wp-json/wp/v2/works?_embed")
      .then(response => {
        this.works = response.reverse();
      })
      .catch(e => {
        this.errors.push(e);
      });
  }
};
</script>

<style lang="scss">
.works {
  padding-bottom: 20px;
  @include tablet {
    padding-bottom: 50px;
  }
  @include desktop-l {
    margin-top: -40px;
  }
}
.works__list {
    display: flex;
    overflow: hidden;
    flex-wrap: wrap;
    margin: -14px -7px 0;
}

.works__item {
    padding: 14px 7px 0;
    width: 100%;
    @include desktop-s {
      width: 50%;
    }
    &--small {
      @include desktop-s {
        width: 33.333%;
      }
    }
    a {
      display: block;
    }
    img {
      display: block;
      width: 100%;
      height: auto;
    }
}

.works__link {
    @include desktop-s {
      &:hover {
        .progressive-image-main {
          transform: scale(1.1);
        }
      }
    }
}
</style>

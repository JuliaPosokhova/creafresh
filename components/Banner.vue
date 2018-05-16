<template>
  <section class="banner">
    <div class="banner__bg">
      {{bannerData.background_text}}
    </div>
    <div class="container">
      <div class="banner__text">
        <h1 class="banner__title ">
          {{bannerData.title}}
        </h1>
        <p class="banner__description">
          {{bannerData.description}}
        </p>
      </div>
      <img :src="image.url" class="banner__image">
    </div>
  </section>
</template>

<script>
export default {
  data: () => ({
    bannerData: {},
    image: {}
  }),

  created() {
    this.$axios
      .$get("https://creafresh.markupus.tech/wp-json/wp/v2/pages/23/?_embed")
      .then(response => {
        this.bannerData = response.acf.modules[0].hero;
        this.image = response.acf.modules[0].hero.image;
      });
  }
};
</script>


<style lang="scss" scoped>
.banner {
  position: relative;
  overflow: hidden;
  height: 360px;
  padding-top: 78px;
  margin-bottom: 18px;
  @include desktop-s {
    min-height: 668px;
    margin-bottom: 0;
  }
  @include desktop-m {
    min-height: 906px;
    margin-bottom: 18px;
  }
  @include desktop-l {
    margin-bottom: 0px;
    min-height: 1006px;
  }
}

.container {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  @include desktop-s {
    justify-content: flex-start;
  }
  @include desktop-l {
    height: calc(100% - 110px);
  }
}

.banner__bg {
  font-weight: 900;
  font-size: 300px;
  line-height: 300px;
  position: absolute;
  left: -15%;
  top: 50%;
  transform: translateY(-50%);
  color: $dark;
  z-index: -1;
  opacity: 0.05;
  @include tablet {
    left: -8%;
    top: 13%;
    font-size: 400px;
    transform: translateY(0);
  }
  @include desktop-s {
    font-size: 900px;
    line-height: 900px;
    top: -17%;
    font-weight: 700;
    left: -11%;
    letter-spacing: 20px;
  }
  @include desktop-m {
    top: 3%;
    left: -5%;
  }
  @include desktop-l {
    top: 18%;
    left: -3%;
    line-height: 700px;
  }
  @include desktop-w {
    top: 16%;
    left: -2%;
  }
}

.banner__text {
  text-align: center;
  @include tablet {
    padding-top: 20px;
  }
  @include desktop-s {
    text-align: left;
    width: 100%;
    padding-right: 400px;
    padding-top: 0;
  }
}

.banner__title {
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

.banner__description {
  font-size: 24px;
  line-height: 30px;
  font-weight: 700;
  max-width: 80%;
  margin: 0 auto;
  @include tablet {
    font-size: 30px;
    line-height: 48px;
    max-width: 100%;
  }
  @include desktop-m {
    font-size: 40px;
    line-height: 60px;
  }
}

.banner__image {
  max-width: 123px;
  position: absolute;
  right: 0;
  top: 0;
  z-index: -1;
  @include tablet {
    max-width: 150px;
  }
  @include desktop-s {
    max-width: 385px;
    top: 13%;
    right: 5%;
  }
  @include desktop-m {
    max-width: 480px;
    top: 22%;
    right: 4%;
  }
  @include desktop-l {
    max-width: 690px;
    top: 11%;
    right: 3%;
  }
}
</style>

<template>
  <section class="feeds">
    <div class="container">
      <a href="#" class="feeds__title">{{title}}</a>
      <div id="instafeed" class="feeds__list"></div>
    </div>
  </section>
</template>

<script>
import Instafeed from "instafeed.js";
export default {
  data() {
    return {
      title: "",
      userId: "",
      clientId: "",
      accessToken: ""
    };
  },
  props: {
    get: {
      type: String,
      required: true
    },
    resolution: {
      type: String
    },
    sortBy: {
      type: String
    },
    limit: {
      type: Number
    },
    links: {
      type: Boolean
    }
  },
  created() {
    this.$axios
      .$get("https://creafresh.markupus.tech/wp-json/wp/v2/pages/23/?_embed")
      .then(response => {
        let instagramData = response.acf.modules.find(obj => {
          return obj.acf_fc_layout === "instagram_highlight";
        }).instagram_highlight;
        this.title = instagramData.title;
        this.userId = instagramData.config.userid;
        this.clientId = instagramData.config.clientid;
        this.accessToken = instagramData.config.accesstoken;
        const feed = new Instafeed({
          get: this.get,
          userId: this.userId,
          clientId: this.clientId,
          accessToken: this.accessToken,
          resolution: this.resolution,
          template:
            '<div class="feeds__item"><a href="{{link}}" target="_blank" id="{{id}}" class="feeds__link" style="background-image:url({{image}})"></a></div>',
          sortBy: this.sortBy,
          limit: this.limit,
          links: this.links
        });
        feed.run();
      })
      .catch(e => {
        console.log(e);
      });
  }
};
</script>

<style lang="scss">
.feeds {
  padding-bottom: 37px;
  @include tablet {
    padding-top: 50px;
  }
  @include desktop-s {
    padding-bottom: 78px;
  }
}

.feeds__title {
  font-size: 15px;
  text-transform: uppercase;
  font-weight: 700;
  text-align: center;
  text-decoration: none;
  color: $dark;
  display: block;
  text-align: center;
  margin-bottom: 44px;
  @include desktop-s {
    margin-bottom: 48px;
    transition: color 0.3s;
    &:hover {
      color: #c536a5;
    }
  }
}

.feeds__list {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

.feeds__item {
  width: calc(50% - 7px);
  height: 143px;
  margin-bottom: 14px;
  letter-spacing: 1px;
  position: relative;
  overflow: hidden;
  @include tablet {
    height: 288px;
    width: calc(50% - 12px);
    margin-bottom: 24px;
  }
  @include desktop-s {
    height: 173px;
    width: calc(20% - 7px);
  }
  @include desktop-m {
    height: 224px;
    width: calc(20% - 11px);
  }
  @include desktop-l {
    height: 288px;
  }
}

.feeds__link {
  background-position: 50% 50%;
  background-size: cover;
  background-repeat: no-repeat;
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  @include desktop-s {
    transition: transform 0.3s;
    &:hover {
      transform: scale(1.1);
    }
  }
}
</style>

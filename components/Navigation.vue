<template>
  <div class="navigation">
    <svg xmlns="http://www.w3.org/2000/svg" display="none" aria-hidden="true">
      <symbol id="home-icon" viewBox="0 0 42 32">
        <path d="M7.314 16.786v12.765c-0.002 0.031-0.002 0.068-0.002 0.105 0 1.231 0.973 2.235 2.192 2.284l0.004 0h2.258c0.483 0 0.874-0.391 0.874-0.874s-0.391-0.874-0.874-0.874h-2.194c-0.27-0.059-0.469-0.296-0.469-0.58 0-0.021 0.001-0.042 0.003-0.063l-0 0.003v-11.892l11.904-9.616 11.959 9.616v11.95c0.002 0.018 0.003 0.038 0.003 0.059 0 0.284-0.199 0.521-0.465 0.58l-0.004 0.001h-12.937c-0.483 0-0.875 0.392-0.875 0.875s0.392 0.875 0.875 0.875h12.937c1.224-0.049 2.197-1.053 2.197-2.284 0-0.038-0.001-0.075-0.003-0.112l0 0.005v-12.823l-13.687-10.957zM41.691 16.555l-20.681-16.555-20.681 16.555c-0.198 0.157-0.323 0.398-0.323 0.668 0 0.212 0.077 0.406 0.206 0.555l-0.001-0.001c0.155 0.198 0.394 0.325 0.663 0.325 0.212 0 0.406-0.079 0.554-0.209l-0.001 0.001 19.639-15.68 19.648 15.68c0.141 0.107 0.319 0.172 0.511 0.176h0.001c0.283-0.004 0.533-0.139 0.693-0.347l0.002-0.002c0.084-0.131 0.134-0.291 0.134-0.462 0-0.289-0.142-0.545-0.36-0.701l-0.003-0.002z"></path>
      </symbol>
    </svg>
    <div class="container">
      <div class="navigation__list">
        <div class="navigation__item" v-for="(item, index) in items" :key="index">
          <nuxt-link :to="item.object_slug" class="navigation__link" @click.native="closeMenu">{{item.title}}</nuxt-link>
        </div>
      </div>
      <div class="languages">
        <a href="#" class="languages__item">Ru</a>
        <a href="#" class="languages__item is-active">Eng</a>
      </div>
      <div class="navigation__home">
        <nuxt-link to="/" class="home-link" @click.native="closeMenu">
          <svg class="svg-icon" aria-hidden="true">
            <use xlink:href="#home-icon"></use>
          </svg>
        </nuxt-link>
      </div>
      <app-footer/>
    </div>
  </div>
</template>

<script>
import AppFooter from "@/components/Footer.vue";

export default {
  components: {
    AppFooter
  },

  data() {
    return {
      items: [],
      errors: []
    };
  },
  created() {
    this.$axios
      .$get("http://creafresh.markupus.tech/wp-json/wp-api-menus/v2/menus/2")
      .then(response => {
        this.items = response.items;
      })
      .catch(e => {
        this.errors.push(e);
      });
  },
  methods: {
    closeMenu() {
      document.body.classList.remove("is-nav-opened");
    }
  }
};
</script>

<style lang="scss">
.navigation {
  > .container {
    @include tablet {
      position: relative;
    }
    @include desktop-l {
      max-width: 100%;
    }
  }
  .footer {
    .container {
      @include desktop-s {
        padding-left: 0;
        padding-right: 0;
      }
    }
  }
}

.navigation__list {
  text-align: center;
  padding-bottom: 14px;
  @include tablet {
    padding-top: 170px;
    padding-bottom: 135px;
  }
  @include desktop-s {
    padding-top: 44px;
    padding-bottom: 44px;
  }
  @include desktop-m {
    padding-top: 88px;
    padding-bottom: 70px;
  }
  @include desktop-l {
    padding-top: 102px;
    padding-bottom: 98px;
  }
  @include desktop-w {
    padding-top: 404px;
    padding-bottom: 154px;
  }
}

.navigation__link {
  font-size: 30px;
  line-height: 60px;
  font-weight: 500;
  color: $dark;
  text-decoration: none;
  @include tablet {
    font-size: 40px;
    line-height: 72px;
  }
  @include desktop-m {
    font-size: 48px;
    line-height: 120px;
  }
  @extend %underline;
  &::before {
    height: 3px;
  }
  &.nuxt-link-active {
    &::before {
      transform: scale(1);
    }
  }
}

.languages {
  display: flex;
  justify-content: center;
  margin-bottom: 27px;
  @include tablet {
    position: absolute;
    right: 20px;
    top: 0px;
    flex-direction: column;
    margin-bottom: 0;
  }
  @include desktop-s {
    right: 50px;
    top: 17px;
  }
  @include desktop-m {
    top: 22px;
  }
}

.languages__item {
  font-size: 16px;
  text-transform: uppercase;
  color: $dark;
  border: 2px solid $dark;
  text-decoration: none;
  display: block;
  padding: 7px 5px;
  text-align: center;
  min-width: 45px;
  margin-left: 4px;
  margin-right: 4px;
  transition: color 0.5s, background-color 0.5s;
  @include tablet {
    margin: 0 0 9px 0;
  }
  @include desktop-s {
    transition: color 0.3s, background-color 0.3s;
    &:hover {
      color: $light;
      background-color: $dark;
    }
  }
}

.is-active {
  background-color: $dark;
  color: $light;
}

.navigation__home {
  padding-bottom: 36px;
  display: flex;
  justify-content: center;
  @include tablet {
    padding-bottom: 46px;
  }
}

.home-link {
  font-size: 42px;
  color: $dark;
  display: inline-block;
  @include desktop-s {
    transition: color 0.3s;
    &:hover {
      color: $brand-color;
    }
  }
  .svg-icon {
    margin: 0 auto;
  }
}
</style>

<template>
  <div class="page">
    <app-header/>
    <nuxt/>
    <app-footer/>
  </div>
</template>

<script>
import AppHeader from "@/components/Header";
import AppFooter from "@/components/Footer";

export default {
  components: {
    AppHeader,
    AppFooter
  }
};
</script>


<style lang="scss">
html {
  font-family: $primary-font;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
</style>

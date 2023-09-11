<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppIconBanner from "./components/AppIconBanner.vue";
import AppFooterTop from "./components/AppFooterTop.vue";
import AppFooterBottom from "./components/AppFooterBottom.vue";

export default {
  data() {
    return {
      sloganPaperino: "",
    };
  },
  components: {
    AppHeader,
    AppMain,
    AppIconBanner,
    AppFooterTop,
    AppFooterBottom,
  },
};
</script>

<template>
  <AppHeader :slogan="sloganPaperino" />
  <AppMain />
  <AppIconBanner />
  <AppFooterTop />
  <AppFooterBottom />
</template>

<style lang="scss">
@use "./assets/styles/general.scss";
</style>

<script>
// IMPORTVUE COMPONENTS
import HeaderComponent from "./components/Header.vue";
import HeroComponent from "./components/Hero.vue";
import MainComponent from "./components/Main.vue";
import BuyComponent from "./components/Buy.vue";
import FooterTopComponent from "./components/FooterTop.vue";
import FooterBottomComponent from "./components/FooterBottom.vue";
// IMPORT ALL JS LINKS VARI
import {
  LinksMenu,
  CardJs,
  LinksBuy,
  LinksFooterTop,
  SocialLinks,
} from "./js/index.js";

export default {
  data() {
    return {
      LinksMenu,
      CardJs,
      LinksBuy,
      LinksFooterTop,
      SocialLinks,
    };
  },
  components: {
    HeaderComponent,
    HeroComponent,
    MainComponent,
    BuyComponent,
    FooterTopComponent,
    FooterBottomComponent,
  },
};
</script>
<template>
  <HeaderComponent :LinksMenu="LinksMenu"></HeaderComponent>
  <HeroComponent class="m-top"></HeroComponent>
  <MainComponent :CardJs="CardJs"></MainComponent>
  <BuyComponent :LinksBuy="LinksBuy"></BuyComponent>
  <FooterTopComponent :LinksFooterTop="LinksFooterTop"></FooterTopComponent>
  <FooterBottomComponent :SocialLinks="SocialLinks"></FooterBottomComponent>
</template>

<style lang="scss">
@use "./scrypt/general.scss" as *;
@use "./scrypt/parzials/mixins" as *;
</style>

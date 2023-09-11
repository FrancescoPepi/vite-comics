<script>
import HeaderComponent from "./components/Header.vue";
import HeroComponent from "./components/Hero.vue";
import MainComponent from "./components/Main.vue";
import BuyComponent from "./components/Buy.vue";
import FooterTopComponent from "./components/FooterTop.vue";
import FooterBottomComponent from "./components/FooterBottom.vue";

export default {
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
  <HeaderComponent></HeaderComponent>
  <HeroComponent class="m-top"></HeroComponent>
  <MainComponent></MainComponent>
  <BuyComponent></BuyComponent>
  <FooterTopComponent></FooterTopComponent>
  <FooterBottomComponent></FooterBottomComponent>
</template>

<style lang="scss">
@use "./scrypt/general.scss" as *;
@use "./scrypt/parzials/mixins" as *;

body {
  font-family: "Signika Negative", sans-serif;
  font-weight: 600;
  font-size: 10px;

  .m-top {
    margin-top: 100px;
  }
  .container {
    margin: auto;
    width: 80%;
  }
}
</style>

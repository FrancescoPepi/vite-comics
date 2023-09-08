<script>
import HeaderComponent from "./components/Header.vue";
import MainComponent from "./components/Main.vue";
import BuyComponent from "./components/Buy.vue";
import FooterComponent from "./components/Footer.vue";

export default {
  components: {
    HeaderComponent,
    MainComponent,
    BuyComponent,
    FooterComponent,
  },
};
</script>
<template>
  <HeaderComponent></HeaderComponent>
  <MainComponent class="m-top"></MainComponent>
  <BuyComponent></BuyComponent>
  <FooterComponent></FooterComponent>
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

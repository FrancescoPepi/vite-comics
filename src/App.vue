<script>
import HeaderComponent from "./components/Header.vue";
import MainComponent from "./components/Main.vue";

export default {
  components: {
    HeaderComponent,
    MainComponent,
  },
};
</script>
<template>
  <HeaderComponent></HeaderComponent>
  <MainComponent></MainComponent>
</template>

<style lang="scss">
@use "./scrypt/general.scss" as *;

body {
  font-family: "Signika Negative", sans-serif;
  font-weight: 600;
  font-size: 10px;
}
</style>

<script>
export default {
  data() {
    return {
      hero: "/img/jumbotron.jpg",
    };
  },
};
</script>

<template>
  <div class="hero"></div>
</template>

<style lang="scss" scoped>
.hero {
  height: 400px;
  background-image: url("/img/jumbotron.jpg");
  background-position: top;
}
</style>

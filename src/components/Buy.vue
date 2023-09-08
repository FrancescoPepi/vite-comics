<script>
export default {
  data() {
    return {
      msg: "--> Content goes here <--",
      card: [],
    };
  },
};
</script>

<template>
  <div v-show="card.length <= 0">
    <div class="container">
      {{ msg }}
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../scrypt/parzials/mixins.scss" as *;

div {
  @include posizione();
  background-color: #1c1c1cff;
  color: white;
  font-size: 30px;
  min-height: 150px;
}
</style>

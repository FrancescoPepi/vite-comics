<script>
import CardProduct from "./CardProduct.vue";

export default {
  data() {
    return {};
  },
  components: {
    CardProduct,
  },
  props: {
    CardJs: Object,
  },
};
</script>

<template>
  <div class="bg">
    <div class="container">
      <div class="btn series">CURRENT SERIES</div>
      <div class="card-container">
        <CardProduct
          v-for="card in CardJs"
          :key="card.thumb"
          :CardJs="card"
        ></CardProduct>
      </div>
      <div class="btn" @click="">LOAD MORE</div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../scrypt/parzials/mixins.scss" as *;

.bg {
  .btn {
    background-color: #0282f9ff;
    padding: 10px 25px;
    font-size: 15px;
    min-width: 200px;
    text-align: center;
    cursor: pointer;
  }
  .series {
    font-size: 30px;

    position: absolute;
    top: -30px;
    left: 100px;
    z-index: 1;
  }
  position: relative;

  background-color: #1c1c1cff;
  color: white;
  .container {
    flex-wrap: wrap;
    display: flex;
    justify-content: center;
    .card-container {
      flex-wrap: wrap;
      display: flex;
      align-items: baseline;
    }
  }
  padding-top: 30px;
  padding-bottom: 20px;
}
</style>

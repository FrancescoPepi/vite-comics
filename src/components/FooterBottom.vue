<script>
export default {
  data() {
    return {};
  },

  props: {
    SocialLinks: Object,
  },
};
</script>

<template>
  <div class="bg">
    <div class="container">
      <div class="button-box">SIGN-UP NOW!</div>

      <ul>
        <span>FOLLOW US</span>
        <li v-for="(link, index) in SocialLinks" :key="link.index">
          <a :href="link.url">
            <img :src="link.img" alt="" />
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../scrypt/parzials/mixins.scss" as *;

.bg {
  background-color: #303030ff;
  height: 150px;
}
.active {
  a {
    color: #0282f9ff;
  }
}
div {
  height: 100px;
  @include posizione("between");

  ul {
    color: #0282f9ff;
    font-size: 15px;
    display: flex;
    align-items: center;
    li {
      width: 60px;
      list-style-type: none;
      text-align: center;
      display: block;
      cursor: pointer;
      a {
        color: black;
        text-decoration: none;
        padding: 50px 0;
      }
      &:hover a {
        filter: invert(1);
      }
    }
    #select {
      width: 70px;
      height: 0px;
      position: absolute;
      justify-content: center;
      left: 0;
      top: 43.5px;
      transition: all 0.3s ease-out;
      div {
        box-shadow: 0px 7px 0px 0px #0282f9ff;
        width: 55px;
      }
    }
  }
}
</style>

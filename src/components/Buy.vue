<script>
export default {
  data() {
    return {};
  },
  props: {
    LinksBuy: Object,
  },
};
</script>

<template>
  <div class="bg">
    <div class="container">
      <div class="link">
        <ul v-for="(link, index) in LinksBuy">
          <li>
            <img :src="link.img" alt="" />
            <a :href="link.url">
              {{ link.linkName.toUpperCase() }}
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../scrypt/parzials/mixins.scss" as *;

div.bg {
  background-color: #0282f9ff;
  color: white;
  font-size: 15px;
  .container {
    padding: 25px 0;

    .link {
      @include posizione("around");
      li {
        width: 50px;
        &:hover {
          filter: invert(0.7);
        }
        img {
          width: 100%;
        }
        @include linkStyle();
        a {
          color: white;
        }
      }
    }
  }
}
</style>

<script>
export default {
  data() {
    return {
      img: "/img/dc-logo.png",
      linkActive: 0,
    };
  },
  methods: {
    isLinkActive(link, index) {
      this.linkActive = index;
      setTimeout(() => {
        this.moveBar(index);
      }, 100);
    },
    moveBar(link) {
      const bar = document.getElementById("select");
      bar.style.left = `calc(70px * ${link})`;
      console.log(bar);
    },
  },
  props: {
    LinksMenu: Object,
  },
};
</script>

<template>
  <div class="bg">
    <div class="container">
      <div class="img-box">
        <img :src="img" alt="" />
      </div>

      <ul>
        <li
          v-for="(link, index) in LinksMenu"
          :key="index"
          @click="isLinkActive(link, index)"
          :class="index == linkActive ? 'active' : ''"
          class="menu"
        >
          <a :href="link.url">
            {{ link.text.toUpperCase() }}
          </a>
        </li>
        <div id="select">
          <div></div>
        </div>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../scrypt/parzials/mixins.scss" as *;

.bg {
  background-color: white;
  opacity: 93%;
  position: fixed;
  z-index: 2;
  top: 0;
  left: 0;
  right: 0;
}
.active {
  a {
    color: #0282f9ff;
  }
}
div {
  height: 100px;
  @include posizione("between");
  .img-box {
    height: 100%;
    img {
      width: 60%;
    }
  }
  ul {
    position: relative;
    li {
      width: 70px;
      list-style-type: none;
      text-align: center;
      display: inline-block;
      line-height: 100px;
      cursor: pointer;
      a {
        color: black;
        text-decoration: none;
        padding: 50px 0;
      }
      &:hover a {
        filter: invert(0.4);
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

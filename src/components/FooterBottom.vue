<script>
export default {
  data() {
    return {
      msg: "ciao",
      links: [
        {
          link: "characters",
          url: "#asdsad",
          active: false,
          position: "0px",
        },
        {
          link: "comics",
          url: "#",
          active: false,
          position: "80px",
        },
        {
          link: "movies",
          url: "#",
          active: false,
          position: "0px",
        },
        {
          link: "tv",
          url: "#",
          active: false,
          position: "300px",
        },
        {
          link: "games",
          url: "#",
          active: false,
          position: "400px",
        },
        {
          link: "collectibles",
          url: "#",
          active: false,
          position: "500px",
        },
        {
          link: "videos",
          url: "#",
          active: false,
          position: "600px",
        },
        {
          link: "fans",
          url: "#",
          active: false,
          position: "700px",
        },
        {
          link: "news",
          url: "#",
          active: false,
          position: "800px",
        },
        {
          link: "shop",
          url: "#",
          active: false,
          position: "900px",
        },
      ],
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
          v-for="(link, index) in links"
          @click="isLinkActive(link, index)"
          :class="index == linkActive ? 'active' : ''"
          class="menu"
        >
          <a :href="link.url">
            {{ link.link.toUpperCase() }}
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
  background-color: #303030ff;
  // opacity: 80%;
  // position: fixed;
  // top: 0;
  // left: 0;
  // right: 0;
}
.active {
  // box-shadow: 0 30px 0 -5px #0282f9ff;
  a {
    color: #0282f9ff;
  }
}
div {
  height: 100px;
  @include posizione("between");
  .img-box {
    // @include posizione();
    height: 100%;
    img {
      width: 60%;
    }
  }
  ul {
    position: relative;
    // @include posizione("between");
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

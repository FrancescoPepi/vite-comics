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
        this.prova(index);
      }, 100);
    },
    prova(link) {
      // const active = document.querySelector(".active");
      const bar = document.getElementById("select");
      // const prova = active.getBoundingClientRect();
      // console.log(prova.left.toFixed());
      bar.style.left = `calc(80px * ${link})`;
      console.log(bar.style.left);
    },
  },
};
</script>

<template>
  <div>
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
</template>

<style lang="scss" scoped>
@use "../scrypt/parzials/mixins.scss" as *;

.active {
  // box-shadow: 0 30px 0 -5px #0282f9ff;
  a {
    color: #0282f9ff;
  }
}

div {
  height: 100px;
  @include between();
  .img-box {
    height: 100%;
    img {
      width: 60%;
    }
  }
  ul {
    padding: 0;
    position: relative;
    @include between();
    li {
      width: 80px;
      list-style-type: none;
      // padding: 5px 20px;
      text-align: center;

      a {
        color: black;
        text-decoration: none;
      }
    }
    #select {
      width: 80px;
      /* background-color: red; */
      position: absolute;
      left: 0;
      top: 0;
      height: 50px;
      // transition: all 0.25s ease-in-out;
      transition: all 0.3s ease-out;
      div {
        box-shadow: inset 0px -10px 0px 0px #0282f9;
        width: 60px;
      }
    }
  }
}
</style>

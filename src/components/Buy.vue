<script>
export default {
  data() {
    return {
      msg: "--> Content goes here <--",
      buyArray: [
        {
          linkName: "digital comics",
          url: "#",
          img: "/img/buy-comics-digital-comics.png",
        },
        {
          linkName: "dc merchandise",
          url: "#",
          img: "/img/buy-comics-merchandise.png",
        },
        {
          linkName: "subscription",
          url: "#",
          img: "/img/buy-comics-subscriptions.png",
        },
        {
          linkName: "comic shop locator",
          url: "#",
          img: "/img/buy-comics-shop-locator.png",
        },
        {
          linkName: "dc power visa",
          url: "#",
          img: "/img/buy-dc-power-visa.svg",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="bg">
    <div class="container">
      <div v-show="buyArray.length <= 0">
        {{ msg }}
      </div>
      <div class="link" v-show="buyArray.length > 0">
        <ul v-for="(link, index) in buyArray">
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

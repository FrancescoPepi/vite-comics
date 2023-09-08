<script>
export default {
  data() {
    return {
      links: [
        {
          title: "DC COMICS",
          subLink: [
            "Characters",
            "Comics",
            "Movies",
            "TV",
            "Games",
            "Videos",
            "News",
          ],
        },
        {
          title: "DC",
          subLink: [
            "Terms Of Use",
            "Privacy policy (New)",
            "Ad Choices",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shop Help",
            "Contact Us",
          ],
        },
        {
          title: "SITES",
          subLink: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
        {
          title: "SHOP",
          subLink: ["Shop DC", "Shop DC Collectibles"],
        },
      ],
      imgBg: "/img/footer-bg.jpg",
      img: "/img/dc-logo-bg.png",
    };
  },
};
</script>

<template>
  <div class="bg">
    <div class="container">
      <div class="container-links">
        <div id="links" v-for="link in links">
          <div class="box">
            {{ link.title }}
            <ul>
              <li v-for="subLink in link.subLink">
                {{ subLink }}
              </li>
            </ul>
          </div>
        </div>
      </div>

      <div id="logo">
        <img :src="img" alt="" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.bg {
  height: 350px;
  background-image: url("/img/footer-bg.jpg");
  color: white;
  .container {
    display: flex;
    justify-content: space-between;
    .container-links {
      padding-top: 20px;
      font-size: 15px;
      display: flex;
      flex-wrap: wrap;
      width: 30%;
      #links {
        margin-right: auto;
        width: calc(100% / 3);
        .box {
          li {
            cursor: pointer;
            color: rgb(110, 110, 110);
            list-style: none;
            &:hover {
              color: white;
            }
          }
        }
      }
    }

    #logo {
      position: relative;
      width: 40%;
      height: 350px;
      overflow: hidden;
      img {
        position: absolute;
        bottom: -30%;
        width: 100%;
        display: block;
        object-fit: cover;
      }
    }
  }
}
</style>

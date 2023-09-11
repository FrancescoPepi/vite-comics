<script>
export default {
  data() {
    return {
      imgBg: "/img/footer-bg.jpg",
      img: "/img/dc-logo-bg.png",
    };
  },
  props: {
    LinksFooterTop: Object,
  },
};
</script>

<template>
  <div class="bg">
    <div class="container">
      <div class="container-links">
        <div id="links" v-for="link in LinksFooterTop">
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
  background-size: cover;
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
      width: 40%;
      height: 350px;
      overflow: hidden;
      img {
        position: relative;
        bottom: 15%;
        width: 100%;
        display: block;
        object-fit: cover;
      }
    }
  }
}
</style>

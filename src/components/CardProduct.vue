<script>
// import HeaderComponent from "./components/Header.vue";

export default {
  data() {
    return {
      title: "titolo",
    };
  },

  // 	methods:{
  // 		myMethods(){
  // 			...
  // 		},
  // 	},

  // components: {
  //	MyComponent,
  // },

  props: {
    cards: Object,
  },
};
</script>

<template>
  <div class="card">
    <div class="img-card">
      <img :src="cards.thumb" :alt="cards.series" />
    </div>
    <div class="title">{{ cards.series.toUpperCase() }}</div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  width: calc((100% - 180px) / 6);
  aspect-ratio: 1/1;
  margin: 15px;
  .img-card {
    overflow: hidden;
    width: 100%;
    height: 100%;
    img {
      object-fit: cover;
      width: 100%;
    }
  }

  .title {
    // padding: 10px;
    margin-top: 10px;
    font-size: 15px;
  }
}
</style>

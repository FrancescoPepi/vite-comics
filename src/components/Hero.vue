<script>
// import HeaderComponent from "./components/Header.vue";

export default {
  data() {
    return {
      title: "titolo",
      hero: "/img/jumbotron.jpg",
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

  // 	props:{
  // 		passaggioInfo: stringa,
  //  	 },
};
</script>

<template>
  <div class="hero"></div>
</template>

<style lang="scss" scoped>
.hero {
  height: 400px;
  background-image: url("/img/jumbotron.jpg");
  background-position: top;
}
</style>

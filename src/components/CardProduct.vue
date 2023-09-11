<script>
export default {
  data() {
    return {};
  },

  props: {
    CardJs: Object,
  },
};
</script>

<template>
  <div class="card">
    <div class="img-card">
      <img :src="CardJs.thumb" :alt="CardJs.series" />
    </div>
    <div class="title">{{ CardJs.series.toUpperCase() }}</div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  width: calc((100% - 180px) / 6);
  aspect-ratio: 1/1;
  margin: 25px 15px;
  .img-card {
    overflow: hidden;
    width: 100%;
    transition: 0.5s ease;
    height: 100%;
    img {
      object-fit: cover;
      transition: 0.5s ease;
      width: 100%;
    }
  }

  .title {
    margin-top: 10px;
    font-size: 15px;
  }

  &:hover .img-card {
    transform: scale(1.1);
    border-radius: 15px;
    border: 1px solid white;
    img {
      transform: scale(1.5);
      border-radius: 15px;
    }
  }
}
</style>

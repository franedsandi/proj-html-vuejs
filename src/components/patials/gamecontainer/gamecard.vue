<script>
export default {
  props: {
    item: {
      type: Object,
      required: true,
    },
  },
};
</script>

<template>
  <div class="custom-card">
    <img :src="item.image" :alt="item.name" />
    <div class="info d-flex ">
      <p>{{ item.name }}</p>
      <a :href="item.link">Shop Now</a>
    </div>
  </div>
</template>


<style scoped lang="scss">
@import '../../../scss/partials/vars';
.custom-card {
  position: relative;
  margin-top: 30px;
  margin-bottom: 70px;
  width: calc(100% / 3 - 15px);
  img {
    width: 100%;
  }
  .info {
    position: absolute;
    bottom: 0;
    height: 20%;
    width: 100%;
    background-color: rgba($purple-color, 0.6);
    flex-direction: column;
    justify-content: center;
    padding: 15px;
    line-height: 0.8;
    p {
      color: $white-color;
      font-size: 20px;
      font-weight: bold;
    }
    a {
      color: $yellow-color;
    }
  }
  &:hover .info {
    background-color: darken($purple-color, 2%);
  }
}
</style>
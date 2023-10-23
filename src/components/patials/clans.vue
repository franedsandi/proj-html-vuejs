<template>
  <div class="container d-flex justify-content-around">
    <img v-for="(image, index) in images" :key="index" :src="image" alt="">
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        'img/brand-01.png',
        'img/brand-02.png',
        'img/brand-03.png',
        'img/brand-04.png',
        'img/brand-05.png'
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.container {
  margin: 70px auto 50px;
}
</style>
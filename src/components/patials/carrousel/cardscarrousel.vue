<script>
  import { Swiper, SwiperSlide } from 'swiper/vue';
  import 'swiper/css';
  import 'swiper/css/pagination';
  import card from './cards.vue'

  export default {
    components: {
      Swiper,
      SwiperSlide,
      card
    },
  };
</script>

<template>
  <div class="container">
    <swiper
      :slidesPerView="4"
      :spaceBetween="30"
      :pagination="{clickable: true}"
      class="mySwiper"
    >
      <swiper-slide><card/></swiper-slide>
      <swiper-slide><card/></swiper-slide>
      <swiper-slide><card/></swiper-slide>
      <swiper-slide><card/></swiper-slide>
      <swiper-slide><card/></swiper-slide>
      <swiper-slide><card/></swiper-slide>
      <swiper-slide><card/></swiper-slide>
      <swiper-slide><card/></swiper-slide>
      <swiper-slide><card/></swiper-slide>
    </swiper>
  </div>
</template>

<style lang="scss" scoped>
.container {
  margin: 50px auto;
  .swiper {
    width: 100%;
    height: 100%;
    .swiper-slide {
      text-align: center;
      font-size: 18px;
      display: flex;
      justify-content: center;
      align-items: center;
    }
  }
}
</style>
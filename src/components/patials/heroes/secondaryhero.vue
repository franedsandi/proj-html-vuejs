<script>
import CarrouselItem from "./CarouselItem.vue";

export default {
  components: {
    CarrouselItem,
  },
  data() {
    return {
      carouselItems: [
        {
          name: "Luies Charls",
          designation: "Web Designer",
          image: "img/t5-1-100x100_left.jpg",
          description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit...",
        },
        {
          name: "Luies Charls",
          designation: "Web Designer",
          image: "img/t4-1-100x100_left.jpg",
          description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit...",
        },
        {
          name: "Luies Charls",
          designation: "Web Designer",
          image: "img/t2-1-100x100_left.jpg",
          description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit...",
        },
      ],
    };
  },
};
</script>

<template>
  <div id="myCarousel" class="carousel slide mb-6" data-bs-ride="carousel">
    <div class="carousel-indicators">
      <button
        v-for="(item, index) in carouselItems"
        :key="index"
        type="button"
        :data-bs-target="'#myCarousel'"
        :data-bs-slide-to="index"
        :class="{ active: index === 0 }"
        :aria-label="`Slide ${index + 1}`"
        :aria-current="index === 0 ? 'true' : null"
      ></button>
    </div>
    <div class="carousel-inner">
      <carrousel-item
        v-for="(item, index) in carouselItems"
        :key="index"
        :item="item"
        :index="index"
      ></carrousel-item>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '../../../scss/partials/vars';
.carousel{
  width: 100%;
  height: 560px;
  background-image: url('img/parallax.jpg');
  background-size: cover;
  background-position: center bottom;
  .carousel-indicators {
    text-align: center;
    display: flex;
    justify-content: center;
    padding-bottom:50px ;
    button {
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background-color:  #333;
      display: inline-block;
      margin: 0 5px;
    }
    .active {
      background-color: $yellow-color;
    }
  }
  .container{
    width: 40%;
    height: 530px;
    padding-top: 100px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: $white-color;
    text-align: center;
    h5{
      margin: 30px 0px;
      span{
        color: $yellow-color;
      }
    }
    .user-img{
      position:relative;
      img{
        border: 2px solid $yellow-color;
        border-radius: 50%;
      }
      .quote{
        position: absolute;
        height: 25px;
        width: 25px;
        padding: 5px;
        background-color: $yellow-color;
        top: 0;
        left: 0;
      } 
    }
  }
}
</style>



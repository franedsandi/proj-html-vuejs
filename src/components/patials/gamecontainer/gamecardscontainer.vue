<script>
import CustomCard from "./gamecard.vue";

export default {
  components: {
    CustomCard,
  },
  data() {
    return {
      cardItems: [
        {
          name: "PUBG : Battlegrounds",
          image: "img/category-image-01-446x550_t.jpg",
          link: "#",
        },
        {
          name: "Battlefield 3",
          image: "img/category-image-02-446x550_t.jpg",
          link: "#",
        },
        {
          name: "Jump Force",
          image: "img/category-image-03-446x550_t.jpg",
          link: "#",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="container d-flex justify-content-between">
    <CustomCard v-for="(item, index) in cardItems" :key="index" :item="item" />
  </div>
</template>




<style lang="scss" scoped>
@import '../../../scss/partials/vars';
.custom-card{
  position: relative;
  margin-top:30px ;
  margin-bottom: 70px;
  width:calc(100% / 3 - 15px);
  img{
    width: 100%;
  }
  .info{
    position: absolute;
    bottom: 0;
    height: 20%;
    width: 100%;
    background-color: rgba($purple-color, 0.6);
    flex-direction: column; 
    justify-content: center;
    padding: 15px;
    line-height: 0.8;
    p{
      color: $white-color;
      font-size: 20px;
      font-weight: bold;
    }
    a{
      color: $yellow-color;
    }
  }
  &:hover .info{
    background-color: darken($purple-color, 2%); 
  }
}

</style>

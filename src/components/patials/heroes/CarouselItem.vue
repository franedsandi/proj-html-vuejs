<template>
  <div class="carousel-item" :class="{ active: index === 0 }">
    <div class="container">
      <div class="user-img">
        <img :src="item.image" :alt="item.name" />
        <img class="quote" src="img/quote.png" alt="quote" />
      </div>
      <h5>{{ item.name }} <span>({{ item.designation }})</span></h5>
      <p>{{ item.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      required: true,
    },
    index: {
      type: Number,
      required: true,
    },
  },
};
</script>

<style scoped lang="scss">
@import '../../../scss/partials/vars';
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
</style>
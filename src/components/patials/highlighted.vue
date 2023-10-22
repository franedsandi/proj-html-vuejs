<script>
export default {
  props: {
    image: String,
    alt:  String,
    highlight: String,
    title: String,
  },
};
</script>

<template>
  <div class="game">
    <img :src="image" :alt="alt" />
    <div class="trapecio-rectangular">
    </div>
    <div class="info d-flex">
      <div class="paralelogramo">
        <p>{{ highlight }}</p>
      </div>
      <p>{{ title }}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '../../scss/partials/vars';
.game {
  width: 49%;
  height: 325px;
  position: relative;
  object-fit: contain;
  img {
    width: 100%;
  }
  .trapecio-rectangular {
    display: none;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(103deg, transparent 20%, rgba(248, 248, 252, 0.329) 70%, rgba(248, 248, 252, 0) 70.1%);
  }
  &:hover .trapecio-rectangular {
    display: block;
  }
  .info {
    position: absolute;
    left: 45%;
    top: 0;
    height: 100%;
    width: 55%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    p {
      color: white;
      font-size: 30px;
      line-height: 1;
    }
    .paralelogramo {
      position: relative;
      margin-left: 5px;
      width: 210px;
      height: 30px;
      background-color: $yellow-color;
      transform: skew(-14deg);
      margin-bottom: 20px;
      p {
        position: absolute;
        right: 3px;
        padding: 0;
        transform: skew(14deg);
        color: black;
        font-size: 25px;
        font-weight: bold;
        width: 100%;
        text-align: center;
      }
    }
  }
}
</style>
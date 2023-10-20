<script>
export default {
  data() {
    return {
      activeButtons: [],
    };
  },
  methods: {
    setActiveButton(index) {
      if (this.activeButtons.includes(index)) {
        this.activeButtons = this.activeButtons.filter((i) => i !== index);
      } else {
        this.activeButtons.push(index);
      }
    },
  },
};
</script>

<template>
  <div class="card">
    <img src="img/04-768x768.jpg" alt="">
    <div class="paralelogramo">
      <p>-44%</p>
    </div>
    <div class="info">
      <p>stars</p>
      <p>name</p>
      <p class="price">price</p>
      <div class="options">
        <button
        type="button"
        class="custom-botton"
        :class="{ 'btn-color': activeButtons.includes(0) }"
        @click="setActiveButton(0)">
          <i class="fa-solid fa-bag-shopping"></i>
        </button>
        <button
        type="button"
        class="custom-botton"
        :class="{ 'btn-color': activeButtons.includes(1) }"
        @click="setActiveButton(1)">
          <i class="fa-solid fa-heart"></i>
        </button>
        <button
        type="button"
        class="custom-botton"
        :class="{ 'btn-color': activeButtons.includes(2) }"
        @click="setActiveButton(2)">
          <i class="fa-solid fa-maximize"></i>
        </button>
        <button
        type="button"
        class="custom-botton"
        :class="{ 'btn-color': activeButtons.includes(3) }"
        @click="setActiveButton(3)">
          <i class="fa-solid fa-eye"></i>
        </button>
    </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '../../../scss/partials/vars';
.card {
  background-color: #22162e;
  position: relative;
  margin-bottom: 40px;
  &:hover .price{
    display: none;
  }
  .paralelogramo {
    position: absolute;
    margin: 5%;
    width: 50px;
    height: 30px;
    background-color: $yellow-color;
    transform: skew(-14deg);
    margin-bottom: 20px;
    p {
      position: absolute;
      transform: skew(14deg);
      color: black;
      font-size: 15px;
      font-weight: bold;
      width: 100%;
      text-align: center;
      top: 50%;
      transform: translateY(-50%);
    }
  }
  .info {
    text-align: start;
    color: white;
    background-color: darken($purple-color, 2%); 
    height:120px ;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    p{
      height: 30px;
      padding-left: 15px;
      margin: 0;

    }
    .options{
      display: none;
      .custom-botton {
      border-radius: 0;
      border: 1px solid black;
      background: none;
      color: white;
      width: calc(100% / 4);
      height: 30px;
      }
      .btn-color {
      color: $yellow-color;
      }
    }
  }
  &:hover .options{
    display: block;
  }
}
</style>
<script>
export default {
  data() {
    return {
      items: [
        {
          image: 'img/caravan-white.png',
          alt: 'caravan',
          title: 'Free Delivery',
          description: 'Free Shipping On All Orders',
        },
        {
          image: 'img/bag-white.png',
          alt: 'moneybag',
          title: 'Money Return',
          description: 'Back Guarentee in 7 days',
        },
        {
          image: 'img/%-white.png',
          alt: 'discount',
          title: 'Member Discount',
          description: 'On every order over $130.00',
        },
        {
          image: 'img/back-white.png',
          alt: 'moneyback',
          title: 'Return Policy',
          description: 'Support 24 hours a day',
        },
      ],
    };
  },
  methods: {
    changeImage(index) {
      this.items[index].image = this.items[index].image.replace('-white', '-yellow');
    },
    resetImage(index) {
      this.items[index].image = this.items[index].image.replace('-yellow', '-white');
    },
  },
};
</script>

<template>
  <div class="container">
    <ul class="d-flex align-items-center gap-5">
      <li v-for="(item, index) in items" :key="index" class="d-flex align-items-center" @mouseover="changeImage(index)" @mouseleave="resetImage(index)">
        <span><img :src="item.image" :alt="item.alt"></span>
        <div class="info">
          <p>{{ item.title }}</p>
          <p>{{ item.description }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
@import '../../scss/partials/vars';

.container {
  
  ul {
    list-style: none;
    padding: 0px;
    margin: 0px 15px;
    height: 200px;
    justify-content: center;
    li {
      position: relative;
      display: flex;
      align-items: center;
      padding-right: 10px;
      img{
        height: 40px;
      }
      span {
        color: white;
        font-size: 40px;
        margin-right: 20px;
      }
      .info {
        line-height: 1.5;
        align-self: center;
        p {
          color: grey;
          margin-bottom: 0;
          &:first-child {
            font-weight: bold;
            color: white;
          }
        }
      }
      &:hover span,
      &:hover .info p:first-child {
        color: $yellow-color;
      }
      &::after {
        content: '';
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        right: -20px;
        height: 70%;
        width: 1px;
        background-color: grey;
      }
      &:last-child::after {
        display: none;
      }
    }
  }
}
</style>
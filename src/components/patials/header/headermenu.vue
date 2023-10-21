<script>
export default {
  data() {
    return {
      links: [
        { text: "Home", url: "#" },
        { text: "Shop", url: "#" },
        { text: "Blog", url: "#" },
        { text: "Media", url: "#" },
        { text: "ShortCode", url: "#" },
        { text: "Features", url: "#" }
      ],
      icons: [
        { name: "search", img: "img/search-white.png", alt: "search-icon", hoverImg: "img/search-yellow.png" },
        { name: "user", img: "img/user-white.png", alt: "user-icon", hoverImg: "img/user-yellow.png" },
        { name: "cart", img: "img/cart-white.png", alt: "cart-icon", hoverImg: "img/cart-yellow.png" }
      ]
    };
  }
};
</script>

<template>
  <div class="container d-flex justify-content-between align-items-center">
    <img src="img/mob-logo.png" alt="">
    <ul class="d-flex gap-5">
      <li v-for="(link, index) in links" :key="index"><a :href="link.url">{{ link.text }}</a></li>
    </ul>
    <ul class="d-flex gap-4">
      <li v-for="(icon, index) in icons" :key="index">
        <a href="#">
          <img :src="icon.img" :alt="icon.alt" :class="icon.name + '-icon'">
        </a>
      </li>
      <span>(0) &#163;0.00 </span>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
@import '../../../scss/partials/vars';
  .container{
    height: 80px;
    color: $white-color;
    img{
      width: 200px;
    }
    a{
      color: white;
      text-decoration: none;
      &:hover{
        color: $yellow-color;
      }
    }
    ul{
      font-size: 20px;
      font-weight:500;
      margin: 0;
      list-style: none;
      img{
        height: 20px;
        width: 20px;
        padding: 1px;
      }
      .search-icon:hover {
        content: url('img/search-yellow.png');
      }
      .user-icon:hover {
        content: url('img/user-yellow.png');
      }
      .cart-icon:hover {
        content: url('img/cart-yellow.png');
      }
    }
    span{
      color:$yellow-color;
    }
  }
</style>    
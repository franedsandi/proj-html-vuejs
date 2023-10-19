<script>
export default {

}
</script>

<template>
  <div class="container d-flex justify-content-between align-items-center">
    <img src="img/mob-logo.png" alt="">
    <ul class="d-flex gap-5">
      <li><a href="#">Home</a></li>
      <li><a href="#">Shop</a></li>
      <li><a href="#">Blog</a></li>
      <li><a href="#">Media</a></li>
      <li><a href="#">ShortCode</a></li>
      <li><a href="#">Features</a></li>
    </ul>
    <ul class="d-flex gap-4">
      <li><a href="#"><i class="fa-solid fa-magnifying-glass"></i></a></li>
      <li><a href="#"><i class="fa-regular fa-user"></i></a></li>
      <li><a href="#"><i class="fa-solid fa-bag-shopping"></i></a></li>
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
    };
    span{
      color:$yellow-color;
    }
  }
</style>
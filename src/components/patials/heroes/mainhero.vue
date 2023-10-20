<script>
export default {

}
</script>

<template>
  <div class="hero p-relative">
    <img src="img/re3.jpg" alt="">
    <div class="info p-absolute">
      <div class="paralelogramo">
        <p class="">Upcoming Stock</p>
      </div>
      <p>Resident Evil 3 Remake</p>
      <button type="button" class="btn btn-light"><a href="#"></a>Shop Now</button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '../../../scss/partials/vars';
.hero {
  position: relative;
  img {
    width: 100%;
  }
  .info {
    position: absolute;
    top: 0;
    height: 100%;
    width: 30%;
    margin-left: 14%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    p {
      color: white;
      font-size: 70px;
      font-weight: bold;
      padding-top: 20px;
      line-height: 1;
    }
    button {
      margin-top: 50px;
      border-radius: 0;
      border: 0px;
      width: 120px;
      height: 50px;
      font-weight: 600;
      &:hover {
        background-color: $yellow-color; // Cambiar el color de fondo al amarillo al pasar el ratón por encima
      }
    }
    .paralelogramo {
      position: relative;
      margin-left: 10px;
      width: 210px;
      height: 50px;
      background-color: $yellow-color;
      transform: skew(-14deg);
      p {
        position: absolute;
        top: 12px;
        right: 3px;
        padding: 0;
        position: absolute;
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
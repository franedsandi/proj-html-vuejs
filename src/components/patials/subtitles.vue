<script>
export default {

}
</script>

<template>
  <div class="subtitle text-center">
    <h1>Subtitle</h1>
  </div>
</template>

<style lang="scss" scoped>
@import '../../scss/partials/vars';
.subtitle{
  position: relative;
  color: white;
  h1{
    &::after {
    content: '';
    display: block;
    width: 50px; 
    background-color: $yellow-color;
    height: 2px;
    position: absolute;
    bottom: -15px;
    left: 50%;
    transform: translateX(-50%);
    }
  }
}
</style>
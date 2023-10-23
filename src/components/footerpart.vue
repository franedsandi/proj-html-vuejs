<script>
import mainpart from './footer/mainfooter.vue'
import bottompart from './footer/footerbottom.vue'
export default {
  components: {
    mainpart,
    bottompart,
  }

}
</script>

<template>
  <div class="customised-container">
    <img src="img/footer-bg.png" alt="footer-image">
    <div class="info">
      <mainpart/>
      <bottompart/>
    </div>
    
    
  </div>
</template>

<style lang="scss" scoped>
.customised-container{
  position:relative;
  height: 470px;
  overflow: hidden;
  img{
    width: 100%;
    height: 100%;
  }
  .info{
    position: absolute;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 100%;
  }
}
</style>
<script>
import hero from './patials/hero.vue'
export default {
  name: 'mainpart',
  components: {
    hero,

  }

}
</script>

<template>
  <div class="custom-container">
  <hero/>
  </div>

</template>

<style lang="scss" scoped>
.custom-container{
  overflow: auto;
  height: calc(100vh - 128px);
}
</style>
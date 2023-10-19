<script>
import game from './highlighted.vue'
export default {
  components: {
    game
  }
}
</script>

<template>
  <div class="container d-flex justify-content-between">
    <game/>
    <game/>
  </div>
</template>

<style>
.container{
  margin-bottom: 60px;
}
</style>
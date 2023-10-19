<script>
import hero from './patials/hero.vue'
import policies from './patials/policies.vue'
export default {
  name: 'mainpart',
  components: {
    hero,
    policies,

  }

}
</script>

<template>
  <div class="custom-container">
  <hero/>
  <policies/>
  </div>

</template>

<style lang="scss" scoped>
.custom-container{
  overflow: auto;
  height: calc(100vh - 128px);
}
</style>
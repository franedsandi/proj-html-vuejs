<script>
import hero from './patials/hero.vue'
import policies from './patials/policies.vue'
import highlight from './patials/gameshighlight.vue'
export default {
  name: 'mainpart',
  components: {
    hero,
    policies,
    highlight,

  }

}
</script>

<template>
  <div class="custom-container">
  <hero/>
  <policies/>
  <highlight/>
  </div>

</template>

<style lang="scss" scoped>
.custom-container{
  overflow: auto;
  height: calc(100vh - 128px);
}
</style>
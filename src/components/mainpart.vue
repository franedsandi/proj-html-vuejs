<script>
import hero from './patials/hero.vue'
import policies from './patials/policies.vue'
import highlight from './patials/mainhighlight/gameshighlight.vue'
import subtitle from './patials/subtitles.vue'
import gamecardcontainer from './patials/gamecontainer/gamecardscontainer.vue'
export default {
  name: 'mainpart',
  components: {
    hero,
    policies,
    highlight,
    subtitle,
    gamecardcontainer,
  }

}
</script>

<template>
  <div class="custom-container">
  <hero/>
  <policies/>
  <highlight/>
  <subtitle/>
  <gamecardcontainer/>
  <subtitle/>
  </div>

</template>

<style lang="scss" scoped>
@import '../scss/partials/vars';
.custom-container{
  overflow: auto;
  height: calc(100vh - 128px);
}
</style>
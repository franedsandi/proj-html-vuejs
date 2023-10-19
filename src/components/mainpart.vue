<script>
import hero from './patials/hero.vue'
import policies from './patials/policies.vue'
import highlight from './patials/mainhighlight/gameshighlight.vue'
import subtitle from './patials/subtitles.vue'
import gamecardcontainer from './patials/gamecontainer/gamecardscontainer.vue'
import carrousel from './patials/carrousel/cardscarrousel.vue'
import options from './patials/optionselector.vue'

export default {
  name: 'mainpart',
  components: {
    hero,
    policies,
    highlight,
    subtitle,
    gamecardcontainer,
    options,
    carrousel,
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
  <options/>
  <carrousel/>
  </div>

</template>

<style lang="scss" scoped>
@import '../scss/partials/vars';
.custom-container{
  overflow: auto;
  height: calc(100vh - 128px);
}
</style>
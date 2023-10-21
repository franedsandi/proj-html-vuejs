<script>
import mainhero from './patials/heroes/mainhero.vue'
import policies from './patials/policies.vue'
import game from './patials/highlighted.vue'
import subtitle from './patials/subtitles.vue'
import gamecardcontainer from './patials/gamecontainer/gamecardscontainer.vue'
import carrousel from './patials/carrousel/cardscarrousel.vue'
import options from './patials/optionselector.vue'
import secondaryhero from './patials/heroes/secondaryhero.vue'

export default {
  name: 'mainpart',
  components: {
    mainhero,
    policies,
    game,
    subtitle,
    gamecardcontainer,
    options,
    carrousel,
    secondaryhero
  }

}
</script>

<template>
  <div class="custom-container">
  <mainhero/>
  <policies/>
  <div class="highlight-container d-flex justify-content-between">
    <game/>
    <game/>
  </div>
  <subtitle/>
  <gamecardcontainer/>
  <subtitle/>
  <options/>
  <carrousel/>
  <div class="highlight-container d-flex justify-content-between">
    <game/>
    <game/>
  </div>
  <subtitle/>
  <options/>
  <carrousel/>
  <secondaryhero/>


  </div>

</template>

<style lang="scss" scoped>
@import '../scss/partials/vars';
.custom-container{
  overflow: auto;
  height: calc(100vh - 128px);
}
.highlight-container{
  margin:0 auto 60px ;
  width: 1300px;

}
</style>
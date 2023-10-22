<script>
import mainhero from './patials/heroes/mainhero.vue'
import policies from './patials/policies.vue'
import game from './patials/highlighted.vue'
import subtitle from './patials/subtitles.vue'
import gamecardcontainer from './patials/gamecontainer/gamecardscontainer.vue'
import carrousel from './patials/carrousel/cardscarrousel.vue'
import options from './patials/optionselector.vue'
import secondaryhero from './patials/heroes/secondaryhero.vue'
import events from './patials/Events.vue'

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
    secondaryhero,
    events, 
  },
}
</script>

<template>
  <div class="custom-container">
  <mainhero/>
  <policies/>
  <div class="highlight-container d-flex justify-content-between">
    <game
      image="img/cms-banner-01.jpg"
      alt="First Game"
      highlight="Most Popular"
      title="The Battlefield 4 Naval Strike"
      />
    <game
      image="img/cms-banner-02.jpg"
      alt="Second Game"
      highlight="Lastest Game"
      title="Assassin's Creed Unity Game"
      />
  </div>
  <subtitle 
    title="Special Category"
    />
  <gamecardcontainer/>
  <subtitle
    title="Our Products"
    />
  <options
  :buttons="['Featured', 'New Arrivels', 'Best Sellers']"/>
  <carrousel/>
  <div class="highlight-container d-flex justify-content-between">
    <game
      image="img/cms-banner-03.jpg"
      alt="Third Game"
      highlight="20% Discount"
      title="Dragon's Dogma Video Game"
    />
    <game
      image="img/cms-banner-04.jpg"
      alt="Fourth Game"
      highlight="30% Discount"
      title="World Of Tanks New Game"
    />
  </div>
  <subtitle title="Deal Of The Day"/>
  <options
  :buttons="['1026 Days', '13 Hours', '24 Mins', '17 Secs']"/>
  <carrousel/>
  <secondaryhero/>
  <subtitle title="New Game Blogs"/>
  <events/>


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
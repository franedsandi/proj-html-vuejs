<script>
import headerpart from './components/headerpart.vue'
import mainpart from './components/mainpart.vue'
import footerpart from './components/footerpart.vue'
export default {
  name: 'App',
  components: {
    headerpart,
    mainpart,
    footerpart,
  }

}
</script>

<template>
  <headerpart/>
<!--   <mainpart/>
  <footerpart/> -->
</template>

<style lang="scss">
@use './scss/main.scss'
</style>

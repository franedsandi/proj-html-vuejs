<script>
import headerpart from './components/headerpart.vue'
import mainpart from './components/mainpart.vue'
export default {
  name: 'App',
  components: {
    headerpart,
    mainpart,
  }

}
</script>

<template>
  <headerpart/>
  <mainpart/>
</template>

<style lang="scss">
@use './scss/main.scss'
</style>

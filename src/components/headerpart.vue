<script>
import headertop from './patials/headertop.vue'
import headermenu from './patials/headermenu.vue'

export default {
  name: 'headerpart',
  components: {
    headertop,
    headermenu,
  }

}
</script>

<template>
  <div class="header">
  <headertop/>
  <headermenu/>
  </div>
</template>

<style lang="scss" scoped>
@import '../scss/partials/vars';
.header{
  background-color: $purple-color ;
}
</style>
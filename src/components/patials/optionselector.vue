<script>
export default {
  props: {
    buttons: {
      type: Array,
      required: true
    }
  },
  data() {
    return {
      active: -1,
    };
  },
  methods: {
    toggleColor(index) {
      this.active = this.active === index ? -1 : index;
    },
  },
}
</script>

<template>
  <div class="container d-flex justify-content-center">
    <button
      v-for="(item, index) in buttons"
      :key="index"
      type="button"
      class="custom-button"
      :class="{ 'btn-color': active === index }"
      @click="toggleColor(index)"
    >
      {{ item }}
    </button>
  </div>
</template>



<style lang="scss" scoped>
@import '../../scss/partials/vars';
.container {
  margin-top: 30px;
}

.custom-button {
  border-radius: 0;
  border: 1px solid black;
  background: none;
  padding: 10px 20px;
  color: white;
}

.btn-color {
  color: $yellow-color;
}
</style>
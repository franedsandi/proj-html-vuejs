<script>
export default {
  data() {
    return {
      active: [false, false, false],
    };
  },
  methods: {
    toggleColor(index) {
      this.active = this.active.map((item, i) => (i === index ? true : false));
    },
  },
};
</script>

<template>
  <div class="container d-flex justify-content-center">
    <button
      type="button"
      class="custom-botton"
      :class="{ 'btn-color': active[0] }"
      @click="toggleColor(0)"
    >
      Toggle button
    </button>
    <button
      type="button"
      class="custom-botton"
      :class="{ 'btn-color': active[1] }"
      @click="toggleColor(1)"
    >
      Toggle button
    </button>
    <button
      type="button"
      class="custom-botton"
      :class="{ 'btn-color': active[2] }"
      @click="toggleColor(2)"
    >
      Toggle button
    </button>
  </div>
</template>

<style lang="scss" scoped>
@import '../../scss/partials/vars';
.container {
  margin-top: 30px;
}

.custom-botton {
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
<template>
  <div class="container d-flex justify-content-between align-items-center">
    <div class="help d-flex align-items-center">
      <a href="#">Wishlist(0)</a>
      <div class="dropdown">
        <a class="btn dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
          Need Help ?
        </a>
        <ul class="dropdown-menu">
          <li><a class="dropdown-item" href="#">Action</a></li>
          <li><a class="dropdown-item" href="#">Another action</a></li>
          <li><a class="dropdown-item" href="#">Something else here</a></li>
        </ul>
      </div>
    </div>
    <div class="contacts"><span>Call 24/7 . 800-8754-987</span></div>
  </div>
</template>

<script>
import 'bootstrap'; 

export default {

}
</script>

<style lang="scss" scoped>
@import '../../scss/partials/vars';

.container {
  color: #A79FAE;
  padding: 0px 10px;
  font-size: 13px;

  p {
    margin: 0;
    position: relative; /* Añade una posición relativa al párrafo */
    &::after {
      content: '';
      display: block;
      width: 1px; /* Incrementa el ancho de la línea para que sea visible */
      background-color: #A79FAE;
      height: 80%; /* Asegúrate de que la línea tenga la misma altura que el párrafo */
      position: absolute;
      top: 50%;
      right: -7px;
      transform: translateY(-50%)
    }
  }
  a {
    color: #A79FAE;
    font-size: 13px;
    text-decoration: none;
  }
}

</style>
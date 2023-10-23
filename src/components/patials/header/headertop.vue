<script>
import 'bootstrap'; 

export default {

}
</script>

<template>
  <div class="top">
    <div class="container d-flex justify-content-between align-items-center">
      <div class="help d-flex align-items-center">
        <a class="help" href="#">Wishlist(0)</a>
        <div class="dropdown">
          <a class="btn dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Need Help ?
          </a>
          <ul class="dropdown-menu">
            <li><a class="dropdown-item" href="#">Action</a></li>
          </ul>
        </div>
      </div>
      <div class="contacts"><span>Call 24/7 . 800-8754-987</span></div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '../../../scss/partials/vars';

.top{
  border-bottom: 1px solid #342B3E;
  .container {
  color: #A79FAE;
  padding: 0px 10px;
  font-size: 20px;
  height: 45px;

  a.help {
    margin: 0;
    position: relative;
    margin-right:30px; 

    &::after {
      content: '';
      display: block;
      width: 1px; 
      background-color: #342B3E;
      height: 60%;
      position: absolute;
      top: 50%;
      right: -20px;
      transform: translateY(-50%)
      }
    }
  a {
    color: #A79FAE;
    font-size: 20px;
    text-decoration: none;
    &:hover{
      color: $yellow-color;
      }
    }
  }
}

</style>
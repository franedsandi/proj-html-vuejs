<script>
export default {

}
</script>

<template>
  <div class="container">
    <ul class="d-flex align-items-center justify-content-between gap-4">
      <li class="d-flex align-items-center">
        <span><i class="fa-solid fa-truck-fast"></i></span>
        <div class="info">
          <p>Free Delivery</p>
          <p>Free Shipping On All Orders</p>
        </div>
      </li>
      <li class="d-flex align-items-center">
        <span><i class="fa-solid fa-sack-dollar"></i></span>
        <div class="info">
          <p>Money Return</p>
          <p>Back Guarentee in 7 days</p>
        </div>
      </li>
      <li class="d-flex align-items-center">
        <span><i class="fa-solid fa-percent"></i></span>
        <div class="info">
          <p>Member Discount</p>
          <p>On every order over $130.00</p>
        </div>
      </li>
      <li class="d-flex align-items-center">
        <span><i class="fa-solid fa-hand-holding-dollar"></i></span>
        <div class="info">
          <p>Return Policy</p>
          <p>Support 24 hours a day</p>
        </div>
      </li>
    </ul>
  </div>
</template>



<style lang="scss" scoped>
.container {
  ul {
    list-style: none;
    padding: 0px;
    margin: 0px 15px;
    height: 200px;
    
    li {
      position: relative;
      display: flex;
      align-items: center;
      padding-right: 10px;
      width: 320px;
      span {
        color: white;
        font-size: 40px;
        margin-right: 20px;
      }
      .info {
        line-height: 1.5;
        align-self: center;
        p {
          color: grey;
          margin-bottom: 0;
          &:first-child {
            font-weight: bold;
            color: white;
          }
        }
      }
      &::after {
        content: '';
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        right: 0;
        height: 70%;
        width: 1px; 
        background-color: grey; 
      }
      &:last-child::after{
        display: none;
      }
    }
  }
}
</style>
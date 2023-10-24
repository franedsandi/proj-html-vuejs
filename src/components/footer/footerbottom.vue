<script>
export default {

}
</script>

<template>
  <div class="custom-container">
    <div class="container">
      <p>Copyright 	&#169; 2023 Codezeel</p>
      <div class="payments">
        <img src="img/americanexpress.png" alt="american express">
        <img src="img/anaranjada.png" alt="???">
        <img src="img/maestro.png" alt="maestro">
        <img src="img/paypal.png" alt="paypal">
        <img src="img/visa.png" alt="visa">
        <img src="img/mastercard.png" alt="mastercard">
      </div>
    </div>  
  </div>
</template>
<style lang="scss" scoped>
  .custom-container{
  position: relative; 
  height: 30px;
  color:white;
  &::before{
    content: '';
    height: 1px;
    width: 100%;
    background-color: grey;
    position: absolute; 
    top: 0; 
    left: 0;
  }
  .container{
    display: flex;
    justify-content: space-between;
    height: 30px;
    img{
      height: 100%;
      padding: 5px 2px;
    }
  }
  
}
</style>
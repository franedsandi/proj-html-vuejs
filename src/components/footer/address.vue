<script>
export default {

}
</script>

<template>
<div class="info">
  <h3>Address Info</h3>
  <ul>
    <li class="address">60 29th Street San Francisco,CA 94110
      507-Union Trade Center, United States Of American
    </li>
    <li class="phone">(+00) 123-456-789</li>
    <li class="email">demo@example.com</li>
  </ul>
</div>
<div class="info">
  <h3>Information</h3>
  <ul>
    <li><a href="#">Bookmark</a></li>
    <li><a href="#">Features</a></li>
    <li><a href="#">Sistemap</a></li>
    <li><a href="#">List</a></li>
    <li><a href="#">Contact Us</a></li>

  </ul>
</div>
  <div class="info">
  <h3>Extras</h3>
  <ul>
    <li><a href="#">Delivery</a></li>
    <li><a href="#">Cart</a></li>
    <li><a href="#">Terms conditions</a></li>
    <li><a href="#">My Account</a></li>
    <li><a href="#">About Us</a></li>
  </ul>
</div>
  <div class="info">
  <h3>Our Newsletter</h3>
  <ul>
    <li>There are many variations of passages of form humour or randomised</li>
    <li></li>
    <li>
      <ul>
        <li><a href=""><i class="fa-brands fa-facebook-f"></i></a></li>
        <li><a href=""><i class="fa-brands fa-x-twitter"></i></a></li>
        <li><a href=""><i class="fa-brands fa-google"></i></a></li>
        <li><a href=""><i class="fa-brands fa-skype"></i></a></li>
        <li><a href=""><i class="fa-brands fa-instagram"></i></a></li>
      </ul>
    </li>
  </ul>
</div>  

</template>

<style lang="scss" scoped>
.address:before {
  content: "🏠"; 
  margin-right: 5px;
}

.phone:before {
  content: "📞"; 
  margin-right: 5px;
}

.email:before {
  content: "✉"; 
  margin-right: 5px;
}

</style>
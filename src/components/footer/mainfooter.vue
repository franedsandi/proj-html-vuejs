<script>
export default {
  data() {
    return {
      infoItems: [
        {
          title: "Information",
          items: [
            { text: "Bookmark", link: "#" },
            { text: "Features", link: "#" },
            { text: "Sistemap", link: "#" },
            { text: "List", link: "#" },
            { text: "Contact Us", link: "#" },
          ],
        },
        {
          title: "Extras",
          items: [
            { text: "Delivery", link: "#" },
            { text: "Cart", link: "#" },
            { text: "Terms conditions", link: "#" },
            { text: "My Account", link: "#" },
            { text: "About Us", link: "#" },
          ],
        },
      ],
    };
  },
};
</script>

<template>
  <div class="container d-flex">
    <div class="info">
      <h3>Address Info</h3>
      <ul>
        <li class="address">60 29th Street San Francisco,CA 94110 
          <br>
        507-Union Trade Center, United States Of American</li>
        <li class="phone">(+00) 123-456-789</li>
        <li class="email">demo@example.com</li>
      </ul>
    </div>
    <div v-for="(item, index) in infoItems" :key="index" class="info">
      <h3>{{ item.title }}</h3>
      <ul>
        <li v-for="(listItem, idx) in item.items" :key="idx">
          <a v-if="listItem.link" :href="listItem.link">{{ listItem.text }}</a>
          <span v-else>{{ listItem.text }}</span>
        </li>
      </ul>
    </div>
      <div class="info">
        <h3>Our Newsletter</h3>
        <ul>
          <li>There are many variations of passages of form humour or randomised</li>
          <li></li>
          <li>
            <ul class="social d-flex">
              <li><a href=""><i class="fa-brands fa-facebook-f"></i></a></li>
              <li><a href=""><i class="fa-brands fa-twitter"></i></a></li>
              <li><a href=""><i class="fa-brands fa-google"></i></a></li>
              <li><a href=""><i class="fa-brands fa-skype"></i></a></li>
              <li><a href=""><i class="fa-brands fa-instagram"></i></a></li>
            </ul>
          </li>
        </ul>
      </div>  
    </div>
</template>

<style lang="scss" scoped>
@import '../../scss/partials/vars';
.container{
  margin: 100px auto;
  color: $white-color;
}
.info{
  width: calc(100% / 4);
}
ul{
  list-style: none;
  padding: 0;
  margin: 0;
}
ul.social{
  gap: 10px;
}
a{
  color: $white-color;
  text-decoration: none;
  &:hover{
    color:$yellow-color;
  }
}

li{
  padding: 7px 0;
  margin: 0;
};

.address:before {
  content: "\f3c5";
  font-family: "Font Awesome 5 Free"; 
  margin-right: 5px;
  color: $yellow-color;
}

.phone:before {
  content: "\f095"; 
  font-family: "Font Awesome 5 Free"; 
  margin-right: 5px;
  color: $yellow-color;
}

.email:before {
  content: "\f0e0"; 
  font-family: "Font Awesome 5 Free";
  margin-right: 5px;
  color: $yellow-color;
}
</style>
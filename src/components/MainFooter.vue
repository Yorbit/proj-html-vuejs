<template>
  <footer>
    <div class="container">
      <section class="footer_nav flex">
        <div class="links_zone">
          <img
            src="../assets/img/avada-bakery-logo.png"
            alt="avada-bakery-logo.png"/>
          <ul>
            <li v-for="(element, index) in footerLinks" :key="index">
              <a :href="element.url"> {{ element.text }} </a>
            </li>
            <li>
              <a href="#"><i class="fa-solid fa-cart-shopping"></i></a>
              <section class="order"> 0 </section>
            </li>
          </ul>
        </div>
        <div class="form">
          <h1 class="title">Subscribe to our Newsletter</h1>
          <input type="email" placeholder="Enter email address here*">
          <button class="btn dark">Subscribe</button>
        </div>
      </section>
      <section class="flex">
        <div class="copyright_zone">
            © Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress
        </div>
        <div class="followus_icon">
          <ul>
            <li><a href="#"><i class="fa-brands fa-instagram"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-twitter"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-facebook-f"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-pinterest-p"></i></a></li>
          </ul>
        </div>
      </section>
      <section class="return">
        <a href="#"><i class="fa-solid fa-chevron-up"></i></a>
      </section>
    </div>
  </footer>
</template>

<script>
export default {
  name: "MainFooter",

  data: function () {
    return {
      footerLinks: [
        {
          text: "Shop",
          url: "#",
        },
        {
          text: "About",
          url: "#",
        },
        {
          text: "Gallery",
          url: "#",
        },
        {
          text: "Locations",
          url: "#",
        },
        {
          text: "Journal",
          url: "#",
        },
        {
          text: "Contact",
          url: "#",
        },
        {
          text: "Orders",
          url: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/generals.scss";
section{
 margin-bottom: 2.5rem;
}
.copyright_zone, .followus_icon, 
.links_zone, .form {
  width: 50%;
}
.order{
    display: inline-block;
    text-align: center;
    background-color: rgba($Perfume, 0.1);
    margin-left: 0.5rem;
    width: 30px;
    height: 30px;
    line-height: 30px;
    border-radius: 50%;
    font-size: 1rem;
}
h1{
    padding-top: 20px;
    padding-bottom: 20px;
}
.form, .followus_icon{
  text-align: end;
}
img{
    padding-bottom: 50px;
}
.form input{
    margin-right: 1rem;
    height: 2.3rem;
    padding: 10px;
    width: 400px;
    border-radius: 5px;
}
.copyright_zone{
  color: $Mamba;
  font-size: 12px;
}
li{
    padding-right: 40px;
}
button{
    padding: 12px 20px 12px 20px;
}
.return{
  padding: 1rem;
  background-color: $OuterSpace;
  width: 50px;
  float: right;
  border-radius: 5px;
  a{
    text-decoration: none;
    color: $White;
  }
}
</style>
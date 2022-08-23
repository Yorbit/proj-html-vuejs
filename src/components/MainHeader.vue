<template>
  <header>
    <section class="flex header_areas between">
      <div class="logo_zone">
        <a id="" href="#">
            <img src="../assets/img/avada-bakery-logo.png" alt="Bakery_Logo"/>
        </a>
      </div>
      <div class="links_zone">
        <ul>
          <li v-for="(element, index) in areasHeader" :key="index">
            <a :href="element.url"> {{ element.text }}</a>
          </li>
          <li>
            <a href="#"><i class="fa-solid fa-cart-shopping"></i></a>
          </li>
        </ul>
      </div>
    </section>
    <div class="container">
      <section class="slogan_zone">
        <h6 class="slogan">Fresh & tasty bakery every day</h6>
        <h1>The Perfect Fresh Bread</h1>
        <p class="philosophy">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis
          dolore error itaque quisquam nulla, pariatur sunt minus ad veritatis
          ullam eligendi quos asperiores voluptatum maiores impedit rem ducimus
          corrupti?</p>
        <button class="btn light">Explore our product</button>
      </section>
    </div>
    <section class="label">
      <div>
        <i class="fa-solid fa-folders"></i>
        <h5>Demos</h5>
      </div>
       <div>
         <span class ="super">$</span>
         <span class="sale">39</span>
         <h5>On Sale</h5>
      </div>
    </section>
  </header>
</template>

<script>
export default {
  name: "MainHeader",
  data: function () {
    return {
      areasHeader: [
        {
          text: "Home",
          url: "#",
        },
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
          text: "Location",
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
          text: "My Account",
          url: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/generals.scss";

header {
  background-image: url("../assets/img/hero-header-bakery.jpg");
  height: 83vh;
  padding: 10px 30px;
  background-size: cover;
  background-position: bottom;
}

.header_areas {
  align-items: center;
}

h1{
  line-height: 70px;
}

  ul li {
    color: $MainBrand;
    text-transform: uppercase;
    margin: 1px 16px;
    &:hover a{
      border-bottom: 3px solid $MainBrand;
    }
  }

.slogan_zone {
  margin-top: 10%;
  width: 30%;
  h1 {
    color: $MainBrand;
    font-size: 54px;
    margin: 5px 0;
  }
}

.super{
  vertical-align: super;
  color: lightgreen;
}

.label {
  top: 140px;
  right: 20px;
  position: fixed;
  div {
    cursor: pointer;
    background-color: $White;
    color: $OuterSpace;
    text-align: center;
    display: block;
    width: 55px;
    padding: 10px 0;
    border-radius: 6px;
    margin: 10px 0;
    font-size: 16px;
    box-shadow: 5px 10px 14px $Mamba;
      .sale{
        color: lightgreen;
        font-size: 1.2rem;
        font-weight: bolder;
      }
  }
}
</style>
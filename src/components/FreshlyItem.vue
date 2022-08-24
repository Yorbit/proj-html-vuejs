<template>
  <div class="container flex between">
        <section class="shopping_zone">
        <h1 class="title">
            Find a freshly baked product perfect for you
        </h1>
        <p class="philosophy">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis
            dolore error itaque quisquam nulla, pariatur sunt minus ad veritatis
            ullam eligendi quos asperiores.
        </p>
        <button class="btn dark">Shop All Products</button>
        </section>
        <section class="label_products">
          <div class="flex between">
              <LabelFreshly
              v-for="(product, index) in freshlyProducts"
              :key="index"
              :product="product.img"
              :productTitle="product.title"
              :productPrice="product.price"
              :productPriceKg="product.priceKg"/>
          </div>
            <i class="fa-solid fa-chevron-left arrow"></i>
            <i class="fa-solid fa-chevron-right arrow arrow_right"></i>
        </section>
  </div>
</template>

<script>
import LabelFreshly from "./LabelFreshly.vue";
export default {
  components: {
    LabelFreshly,
  },

  data: function () {
    return {
      freshlyProducts: [
        {
          img: "choco-chip-cookies-200x255.jpg",
          title: "Choco Chip Cookies",
          price: "19.00",
          priceKg: "39.00",
        },
        {
          img: "strawberry-jam-cookies-200x255.jpg",
          title: "Strawberry Jam Cookies",
          price: "24.00",
          priceKg: "62.00",
        },
        {
          img: "strawberry-donut-200x255.jpg",
          title: "Strawberry Donut",
          price: "24.00",
          priceKg: "42.00",
        },
        {
          img: "perfect-macarons-200x255.jpg",
          title: "Perfect Macarons",
          price: "18.00",
          priceKg: "52.00",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/generals.scss";

.shopping_zone{
    width: 30%;
    text-align: center;
    padding-top: 100px;
}

.label_products {
  width: 70%;
}
</style>
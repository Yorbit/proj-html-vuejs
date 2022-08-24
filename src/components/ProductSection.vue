<template>
  <div class="container flex">
    <section class="section_shopping">
      <h6 class="philosophy">Our Products</h6>
      <h1 class="title">
        All our delectable pastries are backed fresh in our Kitchen very morning, and are made
        with all-natural, all organic ingredients.
      </h1>
      <button class="btn dark">Start Shopping</button>
    </section>

    <section class="item_zone">
      <div class="flex">
        <ProductItems
          v-for="(product, index) in products"
          :key="index"
          :product="product.img"
          :productTitle="product.title"
          :productType="product.type"
          :productPrice="product.price"
          :productPriceKg="product.priceKg"/>
      </div>
      <i class="fa-solid fa-chevron-left arrow"></i>
      <i class="fa-solid fa-chevron-right arrow arrow_right"></i>
    </section>
  </div>
</template>

<script>
import ProductItems from "./ProductItems.vue";
export default {
  components: {
    ProductItems,
  },
  data: function () {
    return {
      products: [
        {
          img: "choco-chip-cookies-400x510.jpg",
          title: "Choco Chip Cookies",
          type: "Cookies, Pastries",
          price: "19.00",
          priceKg: "39.00",
        },
        {
          img: "strawberry-jam-cookies-400x510.jpg",
          title: "Strawberry Jam Cookies",
          type: "Cookies, Pastries",
          price: "24.00",
          priceKg: "62.00",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/generals.scss";

h6{
  font-size: 10px;
  text-transform: uppercase;
}

h1{
  font-size: 28px;
}

.flex{
    justify-content: space-between;
}
</style>
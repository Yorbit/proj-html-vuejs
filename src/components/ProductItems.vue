<template>
    <div class="item">
      <img :src="require('../assets/img/' + product)" :alt="productTitle" />
      <span class="info_item">
        <h1>{{ viewElement(productTitle) }}</h1>
        <h4>{{ viewElement(productType) }}</h4>
        <h2>$ {{ viewElement(productPrice) }}- ${{ viewElement(productPriceKg) }}</h2>
      </span>
    </div>
</template>

<script>
export default {
  props: {
    product: String,
    productTitle: String,
    productType: String,
    productPrice: String,
    productPriceKg: String,
  },

  methods:{
    viewElement(element){
      if(element != "" || null){
        return element;
      }
    },
  }
};
</script>

<style lang="scss" scoped>
@import "../styles/generals.scss";
.item {
  cursor: pointer;
  position: relative;
  &:hover .info_item {
    display: block;
  }
  img{
    width: 100%;
    height: 100%;
  }
}
.info_item {
  display: none;
  position: absolute;
  height: 100%;
  width: 100%;
  padding-top: 13rem;
  transform: translate(-50%, -50%);
  background-color: rgba($OuterSpace, 0.4);
  left: 50%;
  top: 50%;
  text-align: center;
  color: $White;
  * {
    margin: 8px 0;
  }
  h2 {
    font-weight: 400;
  }
  h4 {
    font-weight: 100;
  }
}
</style>
<template>
  <div class="label_freshly">
    <div class="img_Freshly">
      <img :src="require('../assets/img/' + product)" :alt="productTitle" />
      <span><h1>SELECT OPTIONS / QUICK VIEW</h1></span>
    </div>
    <div class="info_label_freshly">
      <h1>{{ productTitle }}</h1>
      <h2>${{ productPrice }} - ${{ productPriceKg }}</h2>
    </div>
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
};
</script>

<style lang="scss" scoped>
@import "../styles/generals.scss";

.label_freshly {
  width: 24%;
  cursor: pointer;
    img {
        width: 100%;
    }
    &:hover span {
        display: block;
    }
}

.img_Freshly {
  width: 100%;
  position: relative;
  line-height: 0;
    span {
        transform: translate(-50%, -50%);
        position: absolute;
        top: 50%;
        height: 100%;
        width: 100%;
        left: 50%;
        background-color: rgba($Mamba, 0.5);
        display: none;
        text-align: center;
        h1 {
        color: $White;
        font-size: 12px;
        line-height: 350px;
        }
    }
}

.info_label_freshly {
  color: $MainBrand;
  text-align: center;
  width: 100%;
  font-size: 12px;
    * {
        margin: 8px 0;
    }
    h2 {
        font-weight: 400;
        font-size: 1rem;
    }
}
</style>
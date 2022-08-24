<template>
  <div class="item_special">
    <img
      :src="require('../assets/img/' + SpecialElement)"
      :alt="SpecialTitle"/>
    <div class="item_special_hover">
      <img
        :src="require('../assets/img/' + SpecialElementHover)"
        :alt="titleAlt"/>
      <span class="info_item_special">
        <h6 class="philosophy">{{ titlePhilosophy }}</h6>
        <h1>{{ titleHover }}</h1>
        <button class="btn dark">{{ btn }}</button>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    SpecialElement: String,
    SpecialTitle: String,
    SpecialElementHover: String,
    titleAlt: String,
    titlePhilosophy: String,
    titleHover: String,
    btn: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/generals.scss";
.item_special {
  cursor: pointer;
  position: relative;
  width: 47%;
  img {
    padding-top: 20px;
    object-fit: cover;
    width: 100%;
  }
  &:hover .item_special_hover{
    display: block;
  }
}

.item_special_hover {
  display: none;
  position: relative;
  position: absolute;
  top: 0;
}

.info_item_special {
  top: 50%;
  left: 50%;
  width: 50%;
  position: absolute;
  transform: translate(-50%, -50%);
  text-align: center;
  color: $White;
  * {
    margin: 14px 0;
  }
  h1 {
    font-size: 2.2rem;
  }
  h6 {
    color: $White;
    font-size: 0.8rem;
  }
}
</style>
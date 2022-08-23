<template>
  <div id="app">
    <MainHeader />
    <BaseMain />
    <MainFooter />
  </div>
</template>

<script>
import MainHeader from "./components/MainHeader.vue";
import BaseMain from "./components/BaseMain.vue";
import MainFooter from "./components/MainFooter.vue";

export default {
  name: 'App',
  components: {
    MainHeader,
    BaseMain,
    MainFooter,
  }
}

</script>

<style lang="scss">
@import "./styles/generals.scss";

.container {
  width: 1600px;
  margin: 6rem auto;
}

.slogan{
  margin: 10px 0;
  color: $Mamba;
  text-transform: uppercase;
  font-weight: 400;
  font-size: 14px;
}

.flex{
  display: flex;
}

.between{
  justify-content: space-between;
}

.philosophy {
  margin: 10px 0;
  font-size: 16px;
  color: $Mamba;
}

ul {
  list-style: none;
  li {
    display: inline-block;
    color: $MainBrand;
  }

  a {
    text-decoration: none;
  }
}

.btn {
  cursor: pointer;
  border: 0px solid;
  padding: 10px 20px;
  margin: 10px 0;
  font-weight: 600;
  border-radius: 6px;
}

.light {
  color: $MainBrand;
  background-color: $White;
  &:hover {
    background-color: $MainBrand;
    color: $White;
  }
}

.dark {
  color: $White;
  margin-top: 2.5rem;
  background-color: $MainBrand;
  &:hover {
    color: $MainBrand;
    background-color: $btnInvert;
  }
}

.item_zone {
  position: relative;
  width: 51%;
}

.section_shopping {
  width: 40%;
  align-self: center;
  margin-bottom: 400px;
}

.arrow {
  position: relative;
  cursor: pointer;
  background-color: rgba($MainBrand, 0.5);
  color: $White;
  padding: 20px 10px;
  bottom: 50%;
}

.arrow_right {
  right: 0;
  position: absolute;
}

</style>

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
</style>

<template>
  <div class="order_section">
    <div class="small_zone">
      <section>
        <h6 class="philosophy">TRY OUR SEASONAL PRODUCTS</h6>
        <h1>Order for pick-up or delivery to your home</h1>
        <button class="btn light">Shop Now</button>
      </section>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
@import "../styles/generals.scss";
.order_section {
  background-image: url("../assets/img/call-to-action-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
.small_zone {
  width: 1200px;
  margin: 0 auto;
  section{
    padding: 1rem 0;
  }
  button{
    margin-bottom:100px;
    padding: 13px 30px 13px 30px;
  }
  h6{
    margin-top:100px;
    font-size: 12px;
    font-weight: 500;
  }
  h1 {
    margin: 1rem 0;
    color: $White;
    font-size: 3rem;
    width: 60%;
    margin-bottom: 70px;
  }
}
</style>
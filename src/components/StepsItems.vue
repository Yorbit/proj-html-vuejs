<template>
  <section class="steps_zone">
    <div class="info_steps">
      <div class="zone_img">
        <img :src="require('../assets/img/' + elementImage)" alt="" />
      </div>
      <div class="info">
        <div class="zone_title">
            <h1 class="title_steps">{{ elementTitle }}</h1>
            <h1 class="id_steps">{{ id }}</h1>
        </div>
        <div class="zone_descr">
            <h6 class="steps">{{ titleSteps }}</h6>
            <p>{{ description }}</p>
        </div>  
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    elementImage: String,
    id: String,
    elementImg: String,
    elementTitle: String,
    titleSteps: String,
    description: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/generals.scss";
.steps{
  color: $Mamba;
  padding-bottom: 10px;
}
.steps_zone{
    position: relative;
}
img {
  object-fit: cover;
  width: 100%;
  height: 100%;
}
.zone_img{
  line-height: 0;
}
h6{
  font-weight: 400;
}
.info{
    position: absolute;
    color: $White;
    background-color: rgba($OuterSpace, 0.5);
    height: 100%;
    width: 100%;
    top:0;
    left: 0;
    padding: 50px;
    .zone_title{
        justify-content: space-between;
        display: flex;
    }
    .title_steps{
        float: left;
        width: 60%;
        font-size: 3rem;
    }
    .id_steps{
        text-align: end;
        font-weight: 100;
        font-size: 3rem;
        width: 10%;
    }
    .zone_descr{
        line-height: 25px;
        position: absolute;
        width: 30%;
        bottom: 15%;
    }  
}
.steps_zone:nth-child(1) .title_steps{
    width: 40%;
}
.steps_zone:nth-child(1) .zone_descr{
    right: 5%;
}
</style>
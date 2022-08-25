<template>
  <div class="container box_cit">
    <StepsItems
      v-for="element in elementsProcess"
      :key="element.id"
      :elementImage="element.img"
      :id="element.id"
      :elementImg="element.img"
      :elementTitle="element.title"
      :titleSteps="element.titleSteps"
      :description="element.description"/>
    <section class="steps_zone extra">
      <div class="cit">
        <h6 class="Steps">DONT JUST TAKE OUR WORD FOR IT</h6>
        <h1 class="title">
          "Finally found an alternative to the mass produced products. Something that incorporates real organic
          ingredients, nutrient dense wellness while promoting sustainability and activity."
        </h1>
        <h5>Rachel Cooper, Founder</h5>
      </div>
    </section>
  </div>
</template>

<script>
import StepsItems from "./StepsItems.vue";
export default {
  components: {
    StepsItems,
},

  data: function () {
    return {
      elementsProcess: [
        {
          img: "bakery-process-1.jpg",
          title: "Tell us what you have in mind",
          id: "01",
          titleSteps: "MANUAL INGREDIENTS SELECTION",
          description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae optio expedita deserunt voluptates est iusto consequatur. Iusto quam porro illum deserunt itaque soluta corporis blanditiis placeat. Ratione cumque sequi quo.",
        },
        {
          img: "bakery-process-2.jpg",
          title: "We Start Baking",
          id: "02",
          titleSteps: "SWEET & DELICIOUS",
          description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae optio expedita deserunt voluptates est iusto consequatur. Iusto quam porro illum deserunt itaque soluta corporis blanditiis placeat. Ratione cumque sequi quo.",
        },
        {
          img: "bakery-process-3.jpg",
          title: "Delivered to your home",
          id: "03",
          titleSteps: "BAKED TO ORDER & GIFT WRAPPED",
          description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae optio expedita deserunt voluptates est iusto consequatur. Iusto quam porro illum deserunt itaque soluta corporis blanditiis placeat. Ratione cumque sequi quo.",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../styles/generals.scss";
.box_cit {
  position: relative;
}
.steps_zone {
  margin: 30px 0;
}
.extra {
  height: 615px;
  margin: 65px 0;
  background-color: rgba($PearlBush, 0.6);
    .cit{
        margin: 100px auto;
        width: 70%;
            h5{
                font-weight: 400;
                padding-top: 20px;
                color: $Mamba;
            }
            h6{
                padding-bottom: 30px;
                color: $Mamba;
            }
    }
}
.steps_zone:nth-child(2),
.steps_zone:nth-child(4) {
  width: 49%;
}
.steps_zone:nth-child(4) {
  right: 0;
  top: 30%;
  position: absolute;
}
</style>
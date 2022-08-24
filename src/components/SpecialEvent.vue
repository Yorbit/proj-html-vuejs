<template>
  <div class="container">
    <section class="title_zone">
        <h6 class="philosophy">CORPORATE & WEDDING</h6>
        <h1 class="title">Baking special Moments</h1>
    </section>

    <section class="items_inline flex between">
             <ItemSpecialEvent v-for="(element, index) in specialElements" 
            :key="index"
            :SpecialElement="element.img"
            :SpecialTitle="element.title"
            :SpecialElementHover="element.imgHover"
            :titleAlt="element.titleAlt"
            :titlePhilosophy="element.titlePhilosophy"
            :titleHover="element.titleHover"
            :btn="element.btn"/>
    </section>
  </div>
</template>

<script>
import ItemSpecialEvent from "./ItemSpecialEvent.vue";
export default {

components: {
    ItemSpecialEvent,
},
  data: function () {
    return {
      specialElements:[
        {
            img:"corporate-bg.jpg",
            title:"corporate.jpg",
            imgHover:"corporate-hover-bg.jpg", 
            titleAlt:"corporate-hover.jpg",
            titlePhilosophy:"International Bakery",
            titleHover:"Corporate Events",
            btn: "Explore More",
        },
        {
            img:"wedding-bg.jpg",
            title:"wedding.jpg",
            imgHover:"wedding-hover-bg.jpg",
            titleAlt:"wedding-hover.jpg",
            titlePhilosophy:"Private Dining Hall",
            titleHover:"Weddings & Parties",
            btn:"Explore More",
        },
      ],
    };
  },
}
</script>
<style lang="scss" scoped>

h1, h6{
    text-align: center;
    padding-bottom: 20px;
}

h6{
    font-size: 12px;
}

</style>
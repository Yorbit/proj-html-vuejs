<template>
    <div id="location" class="container">
        <section class="title_zone">
        <h6 class="philosophy">LOCATIONS</h6>
        <h1 class="title">Visit our Bakeries</h1>
        </section>
        <section class="flex between">
            <ItemLocation v-for="(element, index) in elementsLocation"
            :key="index"
            :image="element.img"
            :country="element.country"
            :phone="element.phoneNumber"
            :hours="element.workingHours"/>
        </section>
    </div>
</template>

<script>
import ItemLocation from './ItemLocation.vue';
export default {
    components:{
        ItemLocation,
    },
  data: function () {
    return {
      elementsLocation: [
        {
          img: "new-york-bk-800x530.jpg",
          country: "New York",
          workingHours: "9:00 AM - 6:00 PM",
          phoneNumber: "1.800.458.556",
        },
         {
          img: "london-bk-800x530.jpg",
          country: "London",
          workingHours: "9:00 AM - 6:00 PM",
          phoneNumber: "1.800.458.556",
        },
      ],
    };
  },
};
</script>
<style scoped lang="scss">
h1, h6{
    margin: 40px 0;
    text-align: center;
}
</style>
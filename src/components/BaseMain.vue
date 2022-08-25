<template>
  <main>
    <ProductSection />
    <SpecialEvent />
    <FreshlyItem />
    <BakerySteps />
    <LocationSection />
    <SocialSection />
  </main>
</template>

<script>
import ProductSection from './ProductSection.vue';
import SpecialEvent from './SpecialEvent.vue';
import FreshlyItem from './FreshlyItem.vue';
import BakerySteps from './BakerySteps.vue';
import LocationSection from './LocationSection.vue';
import SocialSection from './SocialSection.vue';

export default {
    name: 'BaseMain',
    components: {
    ProductSection,
    SpecialEvent,
    FreshlyItem,
    BakerySteps,
    LocationSection,
    SocialSection,
}
}
</script>

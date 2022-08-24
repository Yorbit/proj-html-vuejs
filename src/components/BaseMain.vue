<template>
  <main>
    <ProductSection />
    <SpecialEvent />
    <FreshlyItem />
    <BakerySteps />
  </main>
</template>

<script>
import ProductSection from './ProductSection.vue';
import SpecialEvent from './SpecialEvent.vue';
import FreshlyItem from './FreshlyItem.vue';
import BakerySteps from './BakerySteps.vue';

export default {
    name: 'BaseMain',
    components: {
    ProductSection,
    SpecialEvent,
    FreshlyItem,
    BakerySteps,
    }
}
</script>

<template>
  <main>
    <ProductSection />
    <SpecialEvent />
    <FreshlyItem />
  </main>
</template>

<script>
import ProductSection from './ProductSection.vue';
import SpecialEvent from './SpecialEvent.vue';
import FreshlyItem from './FreshlyItem.vue';

export default {
    name: 'BaseMain',
    components: {
    ProductSection,
    SpecialEvent,
    FreshlyItem,
}
}
</script>

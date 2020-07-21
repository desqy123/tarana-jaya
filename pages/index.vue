<template>
  <div>
    <Carousel />
    <MiniAbout />
    <div class="container mx-auto">
      <OurValue />
      <ProductServices />
      <ProductGallery />
    </div>
  </div>
</template>

<script>
import Carousel from '@/components/Home/Carousel.vue'
import MiniAbout from '@/components/Home/MiniAbout.vue'
import OurValue from '@/components/Home/OurValue.vue'
import ProductServices from '@/components/Home/ProductServices.vue'
import ProductGallery from '@/components/Home/ProductGallery.vue'
export default {
  components: {
    Carousel,
    MiniAbout,
    OurValue,
    ProductServices,
    ProductGallery,
  },
}
</script>

<style>
.serif {
  font-family: 'Zilla Slab', serif;
}

/* [x-cloak] {
  display: none;
} */

.grid-indigo {
  background-image: radial-gradient(#5a67d8 2px, transparent 2px);
  background-size: 16px 16px;
}
</style>

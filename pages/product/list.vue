<template>
  <div>
    <HeaderBanner />
    <div class="container mx-auto px-4">
      <ProductHeading />
      <ProductContent />
      <ProductDetailDownload />
      <Product />
      <Portfolio />
    </div>
    <ProductContact />
  </div>
</template>

<script>
import HeaderBanner from '@/components/HeaderBanner.vue'
import ProductHeading from '@/components/Product/ProductHeading.vue'
import ProductContent from '@/components/Product/ProductContent.vue'
import ProductDetailDownload from '@/components/Product/ProductDetailDownload.vue'
import Product from '@/components/Product/Product.vue'
import Portfolio from '@/components/Product/Portfolio.vue'
import ProductContact from '@/components/Product/ProductContact.vue'
export default {
  components: {
    HeaderBanner,
    ProductHeading,
    ProductContent,
    ProductDetailDownload,
    Product,
    Portfolio,
    ProductContact,
  },
}
</script>

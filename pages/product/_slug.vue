<template>
  <div>
    <HeaderBanner :header-img="productDetail.header_banner" />
    <div class="container mx-auto px-4">
      <ProductHeading
        :title="productDetail.title"
        :description="productDetail.description"
      />
      <ProductContent
        v-if="productDetail.show_content"
        :product-content-list="productDetail.product_content"
      />
      <ProductDetailDownload v-if="productDetail.show_detail" />
      <Product :items="productDetail.items" />
      <Portfolio
        v-if="productDetail.portfolios.length > 0"
        :portfolios="productDetail.portfolios"
      />
    </div>
    <ProductContact />
  </div>
</template>

<script>
import { mapState, mapActions } from 'vuex'
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
  computed: {
    ...mapState('product', ['productDetail']),
  },
  mounted() {
    const routerParams = this.$route.params.slug
    this.getProduct(routerParams)
  },
  methods: {
    ...mapActions('product', ['getProduct']),
  },
}
</script>

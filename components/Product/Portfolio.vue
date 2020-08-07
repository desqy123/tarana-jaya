<template>
  <section class="py-12 px-4">
    <h2 class="text-4xl text-center mb-4 font-semibold">Product Gallery</h2>
    <p class="max-w-2xl mb-8 mx-auto text-center text-gray-800 leading-relaxed">
      We provide the best for you with all my heart.
    </p>
    <div class="flex flex-wrap -mx-4 -mb-8">
      <div
        v-for="(portfolio, key) in portfolios"
        :key="key"
        class="md:w-1/3 px-4 mb-8"
      >
        <video
          v-if="portfolio.type == 'video'"
          controls
          class="rounded shadow-md"
        >
          <source :src="portfolio.portfolio_img" type="video/mp4" />
        </video>
        <img
          v-else=""
          class="rounded shadow-md"
          :src="portfolio.portfolio_img"
          alt=""
        />
      </div>

      <!-- <div class="md:w-1/3 px-4 mb-8">
        <img
          class="rounded shadow-md"
          src="/img/page/product-services/pjuts/portfolio/portfolio-pjuts-2.jpg"
          alt=""
        />
      </div>

      <div class="md:w-1/3 px-4 mb-8">
        <img
          class="rounded shadow-md"
          src="/img/page/product-services/pjuts/portfolio/portfolio-pjuts-3.jpg"
          alt=""
        />
      </div>

      <div class="md:w-1/3 px-4 mb-8">
        <img
          class="rounded shadow-md"
          src="/img/page/product-services/pjuts/portfolio/portfolio-pjuts-4.jpg"
          alt=""
        />
      </div>

      <div class="md:w-1/3 px-4 mb-8">
        <img
          class="rounded shadow-md"
          src="/img/page/product-services/pjuts/portfolio/portfolio-pjuts-5.jpg"
          alt=""
        />
      </div>

      <div class="md:w-1/3 px-4 mb-8">
        <img
          class="rounded shadow-md"
          src="/img/page/product-services/pjuts/portfolio/portfolio-pjuts-6.jpg"
          alt=""
        />
      </div> -->
    </div>
  </section>
</template>
<script>
export default {
  props: {
    portfolios: {
      type: Array,
      required: true,
    },
  },
}
</script>

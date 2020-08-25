<template>
  <section class="py-12 px-4">
    <h2 class="text-5xl mb-2 text-center leading-tight font-bold">
      {{ $t('home.product_services.title') }}
    </h2>
    <p class="text-center mb-12 text-gray-700">
      {{ $t('home.product_services.description') }}
    </p>
    <div>
      <div class="flex flex-wrap flex-row items-center lg:-mx-8 mx-0">
        <div class="md:w-1/2 px-8 mb-8">
          <img
            class="w-4/5 mx-auto"
            src="/img/page/home/home-kontraktor.jpg"
            alt=""
          />
        </div>
        <div class="md:w-1/2 px-8 mb-8">
          <span class="text-4xl font-bold">{{
            $t('home.product_services.pjuts.title')
          }}</span>
          <p class="text-gray-700 leading-relaxed mt-3 mb-5">
            {{ $t('home.product_services.pjuts.description') }}
          </p>
          <button
            class="bg-transparent hover:bg-purple-500 text-purple-700 font-semibold hover:text-white py-2 px-4 border border-purple-500 hover:border-transparent rounded"
          >
            <nuxt-link :to="{ name: 'product-slug', params: { slug: 'PJUTS' } }"
              >View More</nuxt-link
            >
          </button>
        </div>
      </div>
      <div class="flex flex-wrap flex-row items-center lg:-mx-8 mx-0">
        <div class="md:w-1/2 px-8 mb-8 md:order-1">
          <img
            class="w-4/5 mx-auto"
            src="/img/page/home/home-medis.jpg"
            alt=""
          />
        </div>

        <div class="md:w-1/2 px-8 md:text-right">
          <span class="text-4xl font-bold">{{
            $t('home.product_services.medical.title')
          }}</span>
          <p class="text-gray-700 leading-relaxed mt-3 mb-5">
            {{ $t('home.product_services.medical.description') }}
          </p>
          <button
            class="bg-transparent hover:bg-purple-500 text-purple-700 font-semibold hover:text-white py-2 px-4 border border-purple-500 hover:border-transparent rounded"
          >
            <nuxt-link :to="{ name: 'product-slug', params: { slug: 'Medic' } }"
              >View More</nuxt-link
            >
          </button>
        </div>
      </div>
      <div class="flex flex-wrap flex-row items-center lg:-mx-8 mx-0">
        <div class="md:w-1/2 px-8 mb-8 order-none">
          <img
            class="w-4/5 mx-auto"
            src="/img/page/home/home-pendidikan.jpg"
            alt=""
          />
        </div>

        <div class="md:w-1/2 px-8">
          <span class="text-4xl font-bold">{{
            $t('home.product_services.education.title')
          }}</span>
          <p class="text-gray-700 leading-relaxed mt-3 mb-5">
            {{ $t('home.product_services.education.description') }}
          </p>
          <button
            class="bg-transparent hover:bg-purple-500 text-purple-700 font-semibold hover:text-white py-2 px-4 border border-purple-500 hover:border-transparent rounded"
          >
            <nuxt-link
              :to="{ name: 'product-slug', params: { slug: 'Education' } }"
              >View More</nuxt-link
            >
          </button>
        </div>
      </div>
      <div class="flex flex-wrap flex-row items-center lg:-mx-8 mx-0">
        <div class="md:w-1/2 px-8 mb-8 md:order-1">
          <img
            class="w-4/5 mx-auto"
            src="/img/page/home/home-olahraga.jpg"
            alt=""
          />
        </div>

        <div class="md:w-1/2 px-8 md:text-right">
          <span class="text-4xl font-bold">{{
            $t('home.product_services.sport.title')
          }}</span>
          <p class="text-gray-700 leading-relaxed mt-3 mb-5">
            {{ $t('home.product_services.sport.description') }}
          </p>
          <button
            class="bg-transparent hover:bg-purple-500 text-purple-700 font-semibold hover:text-white py-2 px-4 border border-purple-500 hover:border-transparent rounded"
          >
            <nuxt-link :to="{ name: 'product-slug', params: { slug: 'Sport' } }"
              >View More</nuxt-link
            >
          </button>
        </div>
      </div>
      <div class="flex flex-wrap flex-row items-center lg:-mx-8 mx-0">
        <div class="md:w-1/2 px-8 mb-8 order-none">
          <img
            class="w-4/5 mx-auto"
            src="/img/page/home/home-multimedia.jpg"
            alt=""
          />
        </div>

        <div class="md:w-1/2 px-8">
          <span class="text-4xl font-bold">{{
            $t('home.product_services.multimedia.title')
          }}</span>
          <p class="text-gray-700 leading-relaxed mt-3 mb-5">
            {{ $t('home.product_services.multimedia.description') }}
          </p>
          <button
            class="bg-transparent hover:bg-purple-500 text-purple-700 font-semibold hover:text-white py-2 px-4 border border-purple-500 hover:border-transparent rounded"
          >
            <nuxt-link
              :to="{ name: 'product-slug', params: { slug: 'Multimedia' } }"
              >View More</nuxt-link
            >
          </button>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      productServiceList: [],
    }
  },
}
</script>

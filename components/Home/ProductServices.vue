<template>
  <section class="py-12 px-4">
    <h2 class="text-5xl mb-2 text-center leading-tight font-bold">
      Product and Services
    </h2>
    <p class="text-center mb-12 text-gray-700">
      Let’s open a new chapter of your journey!
    </p>
    <div>
      <div class="flex flex-wrap flex-row items-center lg:-mx-8 mx-0">
        <div class="md:w-1/2 px-8 mb-8">
          <img
            class="w-4/5 mx-auto"
            src="img/page/home/home-kontraktor.jpg"
            alt=""
          />
        </div>
        <div class="md:w-1/2 px-8 mb-8">
          <span class="text-4xl font-bold">Solar Public Street Lighting</span>
          <p class="text-gray-700 leading-relaxed mt-3 mb-5">
            Solar Public Street Lighting is a lighting solution for roads and
            areas that are not within the PLN grid area or for lighting cost
            efficiency. Using energy-efficient LED lights with electricity
            supplied from batteries that were previously charged with sunlight
            through solar panels.
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
            src="img/page/home/home-medis.jpg"
            alt=""
          />
        </div>

        <div class="md:w-1/2 px-8 md:text-right">
          <span class="text-4xl font-bold">Medical Supplies</span>
          <p class="text-gray-700 leading-relaxed mt-3 mb-5">
            We also provide medical equipment to support the needs of medical
            personnel in villages and districts in carrying out their duties
            such as Masks, Fogging Composting Devices, Hand Sanitizers, Thermal
            Disinfectant Guns etc.
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
            src="img/page/home/home-pendidikan.jpg"
            alt=""
          />
        </div>

        <div class="md:w-1/2 px-8">
          <span class="text-4xl font-bold">Education Equipment</span>
          <p class="text-gray-700 leading-relaxed mt-3 mb-5">
            Do not forget we also sell textbooks to support the needs of school
            children.
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
            src="img/page/home/home-olahraga.jpg"
            alt=""
          />
        </div>

        <div class="md:w-1/2 px-8 md:text-right">
          <span class="text-4xl font-bold">Sport Equipment</span>
          <p class="text-gray-700 leading-relaxed mt-3 mb-5">
            We offer various kinds of sports equipment to support the needs of
            the community in sports such as Shoes, Badminton Racket, Basketball,
            Volleyball, Table Tennis etc.
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
            src="img/page/home/home-multimedia.jpg"
            alt=""
          />
        </div>

        <div class="md:w-1/2 px-8">
          <span class="text-4xl font-bold">Multimedia Tools</span>
          <p class="text-gray-700 leading-relaxed mt-3 mb-5">
            Do not forget we also sell textbooks to support the needs of school
            children.
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

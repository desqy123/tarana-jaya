<template>
  <section class="px-4">
    <div>
      <div
        v-for="(content, key) in productContentList"
        :key="key"
        class="flex flex-wrap items-center -mx-8"
        :class="{
          'flex-row': isOdd(key),
          'flex-row-reverse': !isOdd(key),
        }"
      >
        <div class="md:w-1/2 px-8 mb-8">
          <img
            v-if="content.product_content_img"
            class="w-4/5 mx-auto"
            :src="content.product_content_img"
            alt=""
          />
        </div>
        <div class="md:w-1/2 px-8 mb-8">
          <span class="text-4xl font-bold">{{
            content.product_content_title
          }}</span>
          <p class="text-gray-700 leading-relaxed mt-3 mb-5">
            E series all in one solar street light design become to the
            revolutionary smart solar light. The whole lamp adopts humanized
            design, combines variety green energy (solar panel, LED light
            source, lithium batteries) as a kit.
          </p>
          <button
            class="bg-transparent hover:bg-purple-500 text-purple-700 font-semibold hover:text-white py-2 px-4 border border-purple-500 hover:border-transparent rounded"
          >
            <a
              href="/img/page/product-services/pjuts/pdf/JIT SUN_E Type(Ver.1)-converted.pdf"
              download
              >Download PDF</a
            >
          </button>
        </div>
      </div>
      <!-- <div class="flex flex-wrap items-center -mx-8">
        <div class="md:w-1/2 px-8 mb-8 md:order-1">
          <img
            class="w-4/5 mx-auto"
            src="/img/page/product-services/pjuts/jitsun-m-type.png"
            alt=""
          />
        </div>

        <div class="md:w-1/2 px-8 md:text-right">
          <span class="text-4xl font-bold">JITSUN M-TYPE</span>
          <p class="text-gray-700 leading-relaxed mt-3 mb-5">
            The whole lamp integrated solar panel, Lithium battery, LED and
            controller together. Smart 6 time-step dimmer and integrated human
            sensor. The latest multi-core LED Chip, make light efficiency
            220lm/W. Real time monitor the weather and battery, more reasonable
            to work.
          </p>
          <button
            class="bg-transparent hover:bg-purple-500 text-purple-700 font-semibold hover:text-white py-2 px-4 border border-purple-500 hover:border-transparent rounded"
          >
            <a
              href="/img/page/product-services/pjuts/pdf/JIT SUN_M Type(Ver.1)-converted.pdf"
              download
              >Download PDF</a
            >
          </button>
        </div>
      </div>
      <div class="flex flex-wrap items-center -mx-8">
        <div class="md:w-1/2 px-8 mb-8 order-none">
          <img
            class="w-4/5 mx-auto"
            src="/img/page/product-services/pjuts/jitsun-s-type.png"
            alt=""
          />
        </div>

        <div class="md:w-1/2 px-8">
          <span class="text-4xl font-bold">JITSUN S-TYPE</span>
          <p class="text-gray-700 leading-relaxed mt-3 mb-5">
            SMART INTEGRATED DESIGN The whole lamp integrated solar panel,
            Lithium battery, LED and controller together. Smart 6 time-step
            dimmer and integrated human sensor. The latest multi-core LED Chip,
            make light efficiency 220lm/W.
          </p>
          <button
            class="bg-transparent hover:bg-purple-500 text-purple-700 font-semibold hover:text-white py-2 px-4 border border-purple-500 hover:border-transparent rounded"
          >
            <a href="/JIT SUN_S Type(Ver.1)-converted.pdf" download
              >Download PDF</a
            >
          </button>
        </div>
      </div> -->
    </div>
  </section>
</template>
<script>
export default {
  props: {
    productContentList: {
      type: Array,
      required: true,
    },
  },
  methods: {
    isOdd(key) {
      return key % 2 === 0
    },
  },
}
</script>

<template>
  <section class="py-12 px-4">
    <h2 class="text-4xl text-center mb-8 font-semibold">Our Product</h2>
    <div class="flex flex-wrap -mx-4">
      <div
        v-for="(item, key) in items"
        :key="key"
        class="w-full lg:w-1/3 px-4 mb-8"
      >
        <div class="relative rounded shadow-md">
          <img :src="item.imgUrl" alt="" />
          <div class="py-4 px-5 border-b">
            <h3 class="text-2xl mb-1 font-bold text-center">
              {{ item.title }}
            </h3>
          </div>
        </div>
      </div>
      <!-- <div class="w-full lg:w-1/3 px-4 mb-8">
        <div class="relative rounded shadow-md">
          <img
            src="/img/page/product-services/pjuts/produksi-tiang-sni.jpg"
            alt=""
          />
          <div class="py-4 px-5 border-b">
            <h3 class="text-2xl mb-1 font-bold text-center">Tiang SNI</h3>
          </div>
        </div>
      </div> -->
    </div>
  </section>
</template>
<script>
export default {
  props: {
    items: {
      type: Array,
      required: true,
    },
  },
}
</script>

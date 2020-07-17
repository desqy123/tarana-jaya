<template>
  <section
    class="text-center lg:bg-top bg-cover"
    :style="{ 'background-image': `url(${headerImg})` }"
  >
    <div class="relative flex items-center py-40">
      <div class="absolute bg-black opacity-50 inset-0"></div>
      <div class="z-10 max-w-2xl mx-auto">
        <h2 class="text-5xl mb-8 leading-tight font-bold text-white my-40"></h2>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    headerImg: {
      type: String,
      required: true,
    },
  },
}
</script>

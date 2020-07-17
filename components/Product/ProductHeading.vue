<template>
  <section class="py-12 px-4 text-center">
    <div class="w-full max-w-2xl mx-auto">
      <h2 class="text-5xl mt-2 mb-6 leading-tight font-bold">
        {{ title }}
      </h2>
      <p class="mb-8 text-gray-700 leading-relaxed">
        {{ description }}
      </p>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      default: '',
    },
  },
}
</script>

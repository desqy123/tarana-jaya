<template>
  <section
    class="bg-cover mx-auto"
    style="background-image: url('/img/page/home/bg/section1.jpg');"
  >
    <div class="py-12 px-4 mb-6">
      <div
        class="flex flex-col lg:flex-row flex-wrap items-center text-center lg:text-left -mx-2 my-20"
      >
        <div class="lg:w-1/2 px-2">
          <img
            class="max-w-custom mx-auto shadow-xl object-cover"
            src="/img/page/home/design-1.jpeg"
            alt=""
          />
        </div>
        <div class="lg:w-1/2 px-2 lg:pr-10 mt-10 lg:mt-0 order-1 lg:order-none">
          <h2
            class="text-5xl mb-6 leading-tight font-heading font-bold heading-custom"
          >
            {{ $t('home.about.title') }}
          </h2>
          <p class="mb-8 text-gray-800 leading-relaxed">
            {{ $t('home.about.description') }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.max-w-custom {
  max-width: 80%;
}

@media (max-width: 414px) {
  .max-w-custom {
    max-width: 90%;
  }

  .heading-custom {
    font-size: 32px;
  }
}
</style>

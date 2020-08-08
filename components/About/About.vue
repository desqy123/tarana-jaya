<template>
  <section class="py-8 px-4 mt-10">
    <div class="flex flex-wrap justify-center lg:justify-between -mx-2">
      <div class="lg:w-2/5 px-2 flex lg:pr-16 mb-6 lg:mb-0">
        <img
          src="/img/logo-tjm.jpeg"
          alt=""
          style="height: 150px;"
          class="mx-auto"
        />
      </div>
      <div class="lg:w-3/5 mx-auto">
        <h2 class="text-4xl font-bold">{{ $t('about.title') }}</h2>
        <p class="text-gray-800 mt-3 text-justify">
          {{ $t('about.description') }}
        </p>
        <button
          class="bg-transparent hover:bg-purple-500 text-purple-700 font-semibold hover:text-white py-2 px-4 border border-purple-500 hover:border-transparent rounded mt-5"
        >
          <a
            href="/img/page/about/Tarana Jaya Mandiri Company Profile.pdf"
            download
            >Download Company Profile</a
          >
        </button>
      </div>
    </div>
  </section>
</template>

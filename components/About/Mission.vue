<template>
  <section class="py-10 px-4">
    <div class="text-center">
      <!-- <span class="text-indigo-600">TAGLINE</span> -->
      <h2 class="text-4xl mt-2 mb-6 leading-tight font-bold">
        {{ $t('about.mission.title') }}
      </h2>
    </div>
    <div class="flex flex-wrap max-w-5xl -mx-4 md:mx-auto -mb-8">
      <div class="w-full md:w-1/2 px-4 mb-8">
        <div
          class="h-full p-6 bg-white rounded border-t-4 border-indigo-500 shadow-md"
        >
          <h3 class="text-2xl mb-3 font-bold">01</h3>
          <p>
            {{ $t('about.mission.list[0].description') }}
          </p>
        </div>
      </div>
      <div class="w-full md:w-1/2 px-4 mb-8">
        <div
          class="h-full p-6 bg-white rounded border-t-4 border-indigo-500 shadow-md"
        >
          <h3 class="text-2xl mb-3 font-bold">02</h3>
          <p>{{ $t('about.mission.list[1].description') }}</p>
        </div>
      </div>
      <div class="w-full md:w-1/2 px-4 mb-8">
        <div
          class="h-full p-6 bg-white rounded border-t-4 border-indigo-500 shadow-md"
        >
          <h3 class="text-2xl mb-3 font-bold">03</h3>
          <p>
            {{ $t('about.mission.list[2].description') }}
          </p>
        </div>
      </div>
      <div class="w-full md:w-1/2 px-4 mb-8">
        <div
          class="h-full p-6 bg-white rounded border-t-4 border-indigo-500 shadow-md"
        >
          <h3 class="text-2xl mb-3 font-bold">04</h3>
          <p>
            {{ $t('about.mission.list[3].description') }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

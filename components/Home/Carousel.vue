<template>
  <div>
    <div v-for="(slider, key) in sliderList" :key="key">
      <transition name="fade" :duration="3000">
        <section
          v-show="key === selectedSlider"
          class="bg-cover lg:bg-center"
          :style="{ 'background-image': `url(${slider.img})` }"
        >
          <div
            v-show="key === selectedSlider"
            class="relative py-8 md:py-24 px-16"
          >
            <div class="absolute inset-0 bg-black opacity-50"></div>
            <div class="z-10 relative w-full">
              <div class="flex flex-col md:flex-row items-center">
                <div
                  class="max-w-sm md:mr-auto text-center md:text-left text-white"
                >
                  <h2
                    class="text-4xl leading-tight font-heading font-bold text-white"
                  >
                    Tarana Jaya Mandiri Membangun Dengan Sepenuh Hati
                  </h2>
                  <p class="my-6 text-gray-300">
                    Tarana Jaya Mandiri merupakan perusahaan Alat Kontraktor,
                    Medis, Pendidikan, Olahraga, dan Multimedia. Telah
                    berpengalaman dan beroperasi sejak tahun 2018. Tarana Jaya
                    Mandiri telah menjadi partner yang terpercaya dibidangnya.
                  </p>
                  <button
                    class="inline-block py-3 px-6 leading-none text-white bg-purple-700 hover:bg-purple-900 rounded shadow"
                  >
                    <a href="contact.html">
                      Contact Us
                    </a>
                  </button>
                </div>
                <div class="mt-8 md:mt-0">
                  <button
                    v-for="(sliderButton, index) in sliderList.length"
                    :key="index"
                    :class="{
                      'bg-indigo-500': index == selectedSlider,
                      'bg-white': index != selectedSlider,
                    }"
                    class="inline-flex md:flex items-center justify-center h-2 w-2 mr-3 mb-4 rounded-full"
                    @click="selectedSlider = index"
                  ></button>
                </div>
              </div>
            </div>
          </div>
        </section>
      </transition>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      selectedSlider: 0,
      sliderList: [
        {
          title: 'Tarana Jaya Mandiri Membangun Dengan Sepenuh Hati',
          subtitle:
            'Tarana Jaya Mandiri merupakan perusahaan Alat Kontraktor, Medis, Pendidikan, Olahraga, dan Multimedia. Telah berpengalaman dan beroperasi sejak tahun 2018. Tarana Jaya Mandiri telah menjadi partner yang terpercaya dibidangnya.',
          button: 'Contact Us',
          showButton: false,
          img: '/img/header/home/header-home.jpeg',
        },
        {
          title: 'Tarana Jaya Mandiri 2',
          subtitle: 'Text 2',
          button: 'About Us',
          showButton: false,
          img: '/img/header/home/header-about.jpeg',
        },
        {
          title: 'Tarana Jaya Mandiri 3',
          subtitle: 'Text 3',
          button: 'Contact Us',
          showButton: true,
          img: '/img/header/home/header-contact.jpeg',
        },
      ],
    }
  },
  mounted() {
    setInterval(() => {
      if (this.selectedSlider === this.sliderList.length - 1) {
        this.selectedSlider = 0
      } else {
        this.selectedSlider += 1
      }
    }, 3000)
  },
  beforeDestroy() {
    clearInterval()
  },
  methods: {
    changeSlider(key) {
      this.selectedSlider = key
    },
  },
}
</script>
<style>
.slide-leave-active,
.slide-enter-active {
  transition: 1s;
}
.slide-enter {
  transform: translate(100%, 0);
}
.slide-leave-to {
  transform: translate(-100%, 0);
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 2s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>

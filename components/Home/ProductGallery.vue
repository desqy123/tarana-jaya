<template>
  <section class="py-12 px-4">
    <h2 class="text-5xl text-center mb-3 font-bold">
      Gallery Product & Services
    </h2>
    <p class="max-w-2xl mb-8 mx-auto text-center text-gray-700 leading-relaxed">
      Become the best and most trusted partner for the progress of your business
    </p>
    <div class="flex max-w-lg mb-12 mx-auto text-center border-b-2">
      <div
        v-for="(galleryCat, key) in galleryCategory"
        :key="key"
        :class="{
          'w-1/3 pb-2 border-b-4 border-indigo-500': key === selectedCategory,
          'w-1/3 pb-2': key !== selectedCategory,
        }"
      >
        <button class="focus:outline-none" @click="changeSelectedCategory(key)">
          {{ galleryCat }}
        </button>
      </div>
      <!-- <div class="w-1/3 pb-2">
        <button class="focus:outline-none">PJUTS</button>
      </div>
      <div class="w-1/3 pb-2">
        <button class="focus:outline-none">Medis</button>
      </div>
      <div class="w-1/3 pb-2 mx-2">
        <button class="focus:outline-none">Pendidikan</button>
      </div>
      <div class="w-1/3 pb-2 mx-2">
        <button class="focus:outline-none">Olahraga</button>
      </div>
      <div class="w-1/3 pb-2">
        <button class="focus:outline-none">Multimedia</button>
      </div> -->
    </div>
    <div class="flex flex-wrap -mx-4 -mb-8">
      <div
        v-for="(gallery, key) in filteredGallery"
        :key="key"
        class="md:w-1/3 px-4 mb-8 content-div"
      >
        <img class="rounded shadow-md" :src="gallery.img" alt="" />
      </div>

      <!-- <div class="md:w-1/3 px-4 mb-8">
        <img class="rounded shadow-md" src="img/gallery/pjuts-2.jpeg" alt="" />
      </div>
      <div class="md:w-1/3 px-4 mb-8">
        <img class="rounded shadow-md" src="img/gallery/pjuts-3.jpeg" alt="" />
      </div>
      <div class="md:w-1/3 px-4 mb-8">
        <img
          class="rounded shadow-md"
          src="img/gallery/olahraga-1.jpeg"
          alt=""
        />
      </div>
      <div class="md:w-1/3 px-4 mb-8">
        <img
          class="rounded shadow-md"
          src="img/gallery/olahraga-2.jpeg"
          alt=""
        />
      </div>
      <div class="md:w-1/3 px-4 mb-8">
        <img
          class="rounded shadow-md"
          src="img/gallery/olahraga-3.jpeg"
          alt=""
        />
      </div>
      <div class="md:w-1/3 px-4 mb-8">
        <img class="rounded shadow-md" src="img/gallery/medic-1.jpeg" alt="" />
      </div>
      <div class="md:w-1/3 px-4 mb-8">
        <img class="rounded shadow-md" src="img/gallery/medic-2.jpeg" alt="" />
      </div>
      <div class="md:w-1/3 px-4 mb-8">
        <img class="rounded shadow-md" src="img/gallery/medic-3.jpeg" alt="" />
      </div> -->
    </div>
  </section>
</template>
<script>
import { mapState } from 'vuex'
export default {
  data() {
    return {
      galleryCategory: [
        'All',
        'PJUTS',
        'Medic',
        'Education',
        'Sports',
        'Multimedia',
      ],
      selectedCategory: 0,
      filteredGallery: [],
      galleryList: [
        {
          name: 'Tiang SNI',
          img: '/img/gallery/pjuts-1.jpeg',
          category: 'PJUTS',
        },
        {
          name: 'Lampu Tenaga Surya',
          img: '/img/gallery/pjuts-2.jpeg',
          category: 'PJUTS',
        },
        {
          name: 'Lampu Tenaga Surya',
          img: '/img/gallery/pjuts-3.jpeg',
          category: 'PJUTS',
        },
        {
          name: 'Sepatu Futsal',
          img: '/img/gallery/olahraga-1.jpeg',
          category: 'Sports',
        },
        {
          name: 'Raket Badminton',
          img: '/img/gallery/olahraga-2.jpeg',
          category: 'Sports',
        },
        {
          name: 'Bola Futsal',
          img: '/img/gallery/olahraga-3.jpeg',
          category: 'Sports',
        },
        {
          name: 'Masker Medis',
          img: '/img/gallery/medic-1.jpeg',
          category: 'Medic',
        },
        {
          name: 'Masker Medis 2',
          img: '/img/gallery/medic-2.jpeg',
          category: 'Medic',
        },
        {
          name: 'Thermometer',
          img: '/img/gallery/medic-3.jpeg',
          category: 'Medic',
        },
        {
          name: 'Pendidikan 1',
          img: '/img/gallery/pendidikan-1.jpg',
          category: 'Education',
        },
        {
          name: 'Pendidikan 2',
          img: '/img/gallery/pendidikan-2.jpg',
          category: 'Education',
        },
        {
          name: 'Pendidikan 3',
          img: '/img/gallery/pendidikan-3.jpg',
          category: 'Education',
        },
        {
          name: 'Multimedia 1',
          img: '/img/gallery/multimedia-1.jpg',
          category: 'Multimedia',
        },
        {
          name: 'Multimedia 2',
          img: '/img/gallery/multimedia-2.png',
          category: 'Multimedia',
        },
        {
          name: 'Multimedia 3',
          img: '/img/gallery/multimedia-3.png',
          category: 'Multimedia',
        },
      ],
    }
  },
  computed: {
    ...mapState('product', ['productList']),
  },
  mounted() {
    this.filteredGallery = this.galleryList
    // eslint-disable-next-line no-console
    // console.log(this.productList)
  },
  methods: {
    changeSelectedCategory(key) {
      this.selectedCategory = key
      if (key !== 0) {
        this.filteredGallery = this.galleryList.filter((value, index) => {
          return value.category === this.galleryCategory[key]
        })
      } else {
        this.filteredGallery = this.galleryList
      }
    },
  },
}
</script>
<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>

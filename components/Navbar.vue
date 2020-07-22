<template>
  <nav class="flex flex-wrap items-center justify-between p-4">
    <div class="flex flex-shrink-0 mr-6">
      <img class="mx-auto w-20" src="/img/logo-tjm.jpeg" alt="" />
    </div>
    <div class="block lg:hidden">
      <button
        class="navbar-burger flex items-center py-2 px-3 text-indigo-500 rounded border border-indigo-500"
      >
        <svg
          class="fill-current h-4 w-4"
          viewbox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <title>Menu</title>
          <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"></path>
        </svg>
      </button>
    </div>
    <div
      class="navbar-menu hidden lg:flex lg:flex-grow lg:items-center w-full lg:w-auto px-2"
    >
      <div class="lg:ml-auto">
        <nuxt-link
          class="block lg:inline-block mt-4 lg:mt-0 mr-10 text-blue-900 hover:text-blue-700 font-bold"
          to="/"
        >
          Home
        </nuxt-link>
        <nuxt-link
          class="block lg:inline-block mt-4 lg:mt-0 mr-10 text-blue-900 hover:text-blue-700 font-bold"
          to="/about"
        >
          About
        </nuxt-link>
        <div
          class="block relative lg:inline-block mt-4 lg:mt-0 mr-10 text-left"
        >
          <div>
            <span class="rounded-md shadow-sm">
              <button
                id="options-menu"
                type="button"
                class="inline-flex w-full px-0 py-0 lg:px-4 lg:py-2 bg-white text-blue-900 hover:text-blue-700 font-bold focus:outline-none focus:border-blue-300 focus:shadow-outline-blue active:bg-gray-50 active:text-gray-800 transition ease-in-out duration-150"
                aria-haspopup="true"
                aria-expanded="true"
                @click="openProduct = !openProduct"
              >
                Product & Services
                <svg
                  class="-mr-1 ml-2 h-5 w-5"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                >
                  <path
                    fill-rule="evenodd"
                    d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                    clip-rule="evenodd"
                  />
                </svg>
              </button>
            </span>
          </div>

          <!--
            Dropdown panel, show/hide based on dropdown state.

            Entering: "transition ease-out duration-100"
              From: "transform opacity-0 scale-95"
              To: "transform opacity-100 scale-100"
            Leaving: "transition ease-in duration-75"
              From: "transform opacity-100 scale-100"
              To: "transform opacity-0 scale-95"
          -->
          <div
            class="origin-top-right absolute right-0 mt-2 w-56 rounded-md shadow-lg z-50"
            :class="{ hidden: !openProduct, block: openProduct }"
            @mouseleave="openProduct = false"
          >
            <div class="rounded-md bg-white shadow-xs">
              <div
                class="py-1"
                role="menu"
                aria-orientation="vertical"
                aria-labelledby="options-menu"
              >
                <nuxt-link
                  v-for="(category, key) in productCategoryList"
                  :key="key"
                  class="block px-4 py-2 text-sm leading-5 text-gray-700 hover:bg-gray-100 hover:text-gray-900 focus:outline-none focus:bg-gray-100 focus:text-gray-900"
                  role="menuitem"
                  :to="{
                    name: 'product-slug',
                    params: { slug: category.name },
                  }"
                  >{{ category.name }}</nuxt-link
                >
              </div>
            </div>
          </div>
        </div>
        <nuxt-link
          class="block lg:inline-block mt-4 lg:mt-0 mr-10 text-blue-900 hover:text-blue-700 font-bold"
          to="/project-list"
        >
          Project List
        </nuxt-link>
        <nuxt-link
          class="block lg:inline-block mt-4 lg:mt-0 mr-10 text-blue-900 hover:text-blue-700 font-bold"
          to="/contact"
        >
          Contact Us
        </nuxt-link>

        <!-- <div
          class="relative block lg:inline-block mt-4 lg:mt-0 mr-10 text-left"
        >
          <div>
            <span class="rounded-md shadow-sm">
              <button
                id="options-menu"
                type="button"
                class="inline-flex justify-start w-full px-0 py-0 lg:px-4 lg:py-2 bg-white text-blue-900 hover:text-blue-700 font-bold focus:outline-none focus:border-blue-300 focus:shadow-outline-blue active:bg-gray-50 active:text-gray-800 transition ease-in-out duration-150"
                aria-haspopup="true"
                aria-expanded="true"
                @click="openLanguage = !openLanguage"
              >
                Language
                <svg
                  class="-mr-1 ml-2 h-5 w-5"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                >
                  <path
                    fill-rule="evenodd"
                    d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                    clip-rule="evenodd"
                  />
                </svg>
              </button>
            </span>
          </div>

          <div
            class="origin-top-right absolute right-0 mt-2 w-56 rounded-md shadow-lg z-50"
            :class="{ hidden: !openLanguage, block: openLanguage }"
            @mouseleave="openLanguage = false"
          >
            <div class="rounded-md bg-white shadow-xs">
              <div
                class="py-1"
                role="menu"
                aria-orientation="vertical"
                aria-labelledby="options-menu"
              >
                <nuxt-link
                  v-for="(picker, key) in languagePicker"
                  :key="key"
                  class="block px-4 py-2 text-sm leading-5 text-gray-700 hover:bg-gray-100 hover:text-gray-900 focus:outline-none focus:bg-gray-100 focus:text-gray-900"
                  role="menuitem"
                  :to="{
                    name: 'language-slug',
                    params: { slug: picker.title },
                  }"
                >
                  <div class="flex flex-row">
                    <img
                      width="24"
                      class="object-cover mr-2"
                      :src="picker.svgImg"
                    />
                    <div>
                      {{ picker.title }}
                    </div>
                  </div>
                </nuxt-link>
              </div>
            </div>
          </div>
        </div> -->
      </div>
    </div>
  </nav>
</template>
<script>
import { mapState } from 'vuex'
export default {
  data() {
    return {
      openProduct: false,
      productCategory: [
        'PJUTS',
        'Medis',
        'Pendidikan',
        'Olahraga',
        'Multimedia',
      ],

      openLanguage: false,
      languagePicker: [
        {
          title: 'Bahasa Indonesia',
          svgImg:
            'https://upload.wikimedia.org/wikipedia/commons/thumb/9/9f/Flag_of_Indonesia.svg/64px-Flag_of_Indonesia.svg.png',
        },
        {
          title: 'English',
          svgImg:
            'https://upload.wikimedia.org/wikipedia/commons/8/83/Flag_of_the_United_Kingdom_%283-5%29.svg',
        },
      ],
    }
  },
  computed: {
    ...mapState('product', ['productCategoryList']),
  },
  mounted() {
    /**
     * Dropdown menu
     */
    // document.addEventListener('DOMContentLoaded', function () {
    const menus = document.querySelectorAll('.navbar-burger')
    const dropdowns = document.querySelectorAll('.navbar-menu')

    if (menus.length && dropdowns.length) {
      for (let i = 0; i < menus.length; i++) {
        menus[i].addEventListener('click', function () {
          for (let j = 0; j < dropdowns.length; j++) {
            dropdowns[j].classList.toggle('hidden')
          }
        })
      }
    }
    // })
  },
}
</script>

<template>
  <section class="py-12 px-4">
    <h2 class="text-4xl mb-12 text-center font-bold">Our Contact</h2>
    <div class="flex flex-wrap -mx-6">
      <div class="w-full lg:w-1/2 px-6 mb-8 lg:mb-0">
        <h3 class="text-2xl mb-10 font-heading">
          We always give the best for you with all my heart
        </h3>
        <ul>
          <li class="mb-2">
            <img
              class="inline-block w-8 h-8 pr-2"
              src="placeholders/icons/home.svg"
              alt=""
            /><span
              >Jln. Pendidikan Desa Tawiri, Kec, Teluk Ambon, Kota Ambon 972,
              Prov, Maluku.</span
            >
          </li>
          <li class="mb-2">
            <img
              class="inline-block w-8 h-8 pr-2"
              src="placeholders/icons/mobile.svg"
              alt=""
            /><span><strong>Phone Office 1 : </strong>081384593862</span>
          </li>
          <li class="mb-2">
            <img
              class="inline-block w-8 h-8 pr-2"
              src="placeholders/icons/mobile.svg"
              alt=""
            /><span><strong>Phone Office 2 : </strong>081388161716</span>
          </li>
          <li class="mb-2">
            <img
              class="inline-block w-8 h-8 pr-2"
              src="placeholders/icons/mobile.svg"
              alt=""
            /><span><strong>Phone Office 3 : </strong>085243444333</span>
          </li>
          <li class="mb-2">
            <img
              class="inline-block w-8 h-8 pr-2"
              src="placeholders/icons/message.svg"
              alt=""
            /><span>info@taranajayamandiri.com</span>
          </li>
        </ul>
      </div>
      <div class="w-full lg:w-1/2 px-6">
        <form>
          <div class="mb-4">
            <input
              class="appearance-none block w-full py-3 px-4 leading-tight text-gray-700 bg-gray-200 focus:bg-white border border-gray-200 focus:border-gray-500 rounded focus:outline-none"
              type="email"
              placeholder="Email"
            />
          </div>
          <div class="mb-4">
            <select
              class="appearance-none block w-full py-3 px-4 leading-tight text-gray-700 bg-gray-200 focus:bg-white border border-gray-200 focus:border-gray-500 rounded focus:outline-none"
            >
              <option>-- Select product --</option>
              <option>Penerangan Jalan Umum Tenaga Surya</option>
              <option>Alat Medis</option>
              <option>Alat Pendidikan</option>
              <option>Alat Olahraga</option>
              <option>Alat Multimedia</option>
            </select>
          </div>
          <div class="mb-4">
            <textarea
              class="appearance-none block w-full py-3 px-4 leading-tight text-gray-700 bg-gray-200 focus:bg-white border border-gray-200 focus:border-gray-500 rounded focus:outline-none"
              placeholder="Write something..."
              rows="5"
            ></textarea>
          </div>
          <div>
            <button
              type="button"
              class="inline-block w-full py-4 px-8 leading-none text-white bg-indigo-500 hover:bg-indigo-600 rounded shadow"
              @click="onContactSubmit"
            >
              Submit
            </button>
          </div>
        </form>
      </div>
    </div>
    <Modal :show.sync="showModal" />
  </section>
</template>
<script>
import Modal from '@/components/Modal.vue'
export default {
  components: {
    Modal,
  },
  data() {
    return {
      showModal: false,
    }
  },
  methods: {
    onContactSubmit() {
      // eslint-disable-next-line no-console
      console.log('asdasd')
      this.showModal = true
    },
  },
}
</script>

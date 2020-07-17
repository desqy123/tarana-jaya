<template>
  <div>
    <HeaderBanner header-img="/img/header/home/header-contact.jpeg" />
    <div class="container mx-auto px-4">
      <Contact />
    </div>
  </div>
</template>

<script>
import HeaderBanner from '@/components/HeaderBanner.vue'
import Contact from '@/components/Contact/Contact.vue'
export default {
  components: {
    HeaderBanner,
    Contact,
  },
}
</script>

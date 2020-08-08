<template>
  <div>
    <HeaderBanner header-img="/img/header/home/header-about.jpeg" />
    <div class="container mx-auto px-4">
      <About />
      <Vision />
      <Mission />
      <!-- <OurTeam /> -->
    </div>
  </div>
</template>

<script>
import HeaderBanner from '@/components/HeaderBanner.vue'
import About from '@/components/About/About.vue'
import Vision from '@/components/About/Vision.vue'
import Mission from '@/components/About/Mission.vue'
// import OurTeam from '@/components/About/OurTeam.vue'
export default {
  components: {
    HeaderBanner,
    About,
    Vision,
    Mission,
    // OurTeam,
  },
}
</script>

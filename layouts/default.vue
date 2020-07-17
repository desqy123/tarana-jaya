<template>
  <div class="bg-body text-body font-body">
    <Navbar />
    <Nuxt />
    <FooterBar />
  </div>
</template>
<script>
import Navbar from '@/components/Navbar.vue'
import FooterBar from '@/components/FooterBar.vue'
export default {
  components: {
    Navbar,
    FooterBar,
  },
}
</script>
<style>
/* .content-div {
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}

.content-div:hover {
  background-image: linear-gradient(
    to right,
    rgba(126, 213, 111, 0.801),
    hsla(160, 64%, 43%, 0.801)
  );
  z-index: 0;
}

.image-cover {
  height: 260px;
} */
</style>

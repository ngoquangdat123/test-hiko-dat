<template>
  <div class="text-white">
    <nuxt />
    <scroll-to-top />
  </div>
</template>

<script>
import ScrollToTop from '../components/ScrollToTop.vue'

export default {
  components: {
    ScrollToTop
  }
}
</script>

<style>
body {
  font-family: Raleway;
  font-size: 16px;
}
.text-white {
  color: #FFFFFF;
}
</style>

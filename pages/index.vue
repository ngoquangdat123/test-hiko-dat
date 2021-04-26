<template>
  <div class="landing-wrapper">
    <the-header/>
    <about/>
    <product/>
    <partner/>
    <our-client/>
    <contact/>
  </div>
</template>

<script>
import TheHeader from '../components/TheHeader.vue'
import About from '../components/About.vue'
import Product from '../components/Product.vue'
import Partner from '../components/Partner.vue'
import OurClient from '../components/OurClient.vue'
import Contact from '../components/Contact.vue'

export default {
  components: {
    TheHeader,
    About,
    Product,
    Partner,
    OurClient,
    Contact
  },
}
</script>

<style lang='scss' scoped>
.landing-wrapper {
  background: #15161E;
  min-height: 100vh;
}
</style>

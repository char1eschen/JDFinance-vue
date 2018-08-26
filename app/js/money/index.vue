<template lang="html">
  <div>
      <Heador/>  
      <Slider/>
      <Ad1/>
      <Money/>
      <Ad2/>
      <Finance/>
      <Ad3/>
      <Footor cname="mfooter"/>
      <Navbar/> 
  </div>
</template>

<script>
  import Heador from '../public/header.vue'
  import Footor from '../public/footer.vue'
  import Navbar from '../public/navbar.vue'
  import Slider from './mslider.vue' 
  import Ad1 from './ad1.vue'
  import Money from './money.vue'
  import Ad2 from './ad2.vue'
  import Finance from './finance.vue'
  import Ad3 from './ad3.vue'
  export default {
    components: {
      Heador,
      Slider,
      Ad1,
      Money,
      Ad2,
      Finance,
      Ad3,
      Footor,
      Navbar
    }
  }
</script>

<style lang="scss">
  .mfooter {
    margin-top: 0!important;
    ul {
      li:first-child {
        display: none;
      }
    }
  }
</style>

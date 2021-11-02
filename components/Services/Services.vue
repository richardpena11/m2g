<template>
  <div class="services_container">
    <div id="services" class="anchor"></div>
    <AllServices />
    <Banner />
    <AllDetailedServices />
  </div>
</template>

<script>
import AllServices from './AllServices/AllServices.vue'
import Banner from './Banner/Banner.vue'
import AllDetailedServices from './DetailedServices/AllDetailedServices.vue'
  export default {
  components: { 
    AllServices,
    Banner,
    AllDetailedServices
  },
    
  }
</script>

<style lang="scss" scoped>

</style>
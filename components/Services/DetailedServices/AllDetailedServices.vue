<template>
  <div class="detailed-services">
    <DetailedService 
      v-for="(detailedService, index) of detailedServices"
      :key="index"
      :service="detailedService"
      :index="index"
    />
  </div>
</template>

<script>
  import DetailedService from './DetailedService.vue'
  export default {
    components: {
      DetailedService
    },
    data() {
      return {
        detailedServices: ["website", "taxes", "finances", "insurance"]
      }
    },
  }
</script>

<style lang="scss" scoped>
  .detailed-services {
    margin-top: 150px;
  }
</style>
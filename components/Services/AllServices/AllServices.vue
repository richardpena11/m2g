<template>
  <div class="all-services">
    <div class="all-services__title">
      <h3 class="all-services__title__main">
        Some kind of subtitle over here
      </h3>
      <h3 class="all-services__title__secondary">
        Some kind of small description can go here but not longer than this.
      </h3>
    </div>
    <div class="all-services__info">
      <Service v-for="(service, index) in services" :key="index" :service="service"/> 
    </div>
  </div>
</template>

<script>
  import Service from './Service'
  export default {
    components: {
      Service
    },
    data() {
      return {
        services: [
          {
            anchor: 'insurance',
            svg: 'insurances.svg',
            title: 'Insurances',
            desc: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc pulvinar blandit commodo. Aenean tristique felis quis orci dignissim.'
          },
          {
            anchor: 'website',
            svg: 'websites.svg',
            title: 'Websites',
            desc: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc pulvinar blandit commodo. Aenean tristique felis quis orci dignissim.'
          },
          {
            anchor: 'taxes',
            svg: 'taxes.svg',
            title: 'Taxes',
            desc: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc pulvinar blandit commodo. Aenean tristique felis quis orci dignissim.'
          },
          {
            anchor: 'finances',
            svg: 'finances.svg',
            title: 'Finances',
            desc: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc pulvinar blandit commodo. Aenean tristique felis quis orci dignissim.'
          },
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
  .all-services {
    padding: 50px 0;
    &__title {
      text-align: center;
      &__main {
        padding-bottom: 20px;
        color: var(--dark-main-color);
        font-size: 26px;
        font-weight: 500;
      }
      &__secondary {
        color: var(--lighter-text-color);
        font-size: 20px;
        font-weight: 300;
      }
    }
    &__info {
      margin: 0 auto;
      width: 100%;
      max-width: 1200px;
      padding-top: 75px;
      display: flex;
      justify-content: space-around;
      flex-wrap: wrap;
    }
  }

  @media screen and (max-width: 1050px) {
    .all-services {
      &__info {
        margin: 0 auto;
        width: 90%;
        max-width: 1200px;
        padding-top: 75px;
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;
      }
    }
  }

  @media screen and (max-width: 800px) {
    .all-services {
      &__title {
        margin: 0 auto;
        width: 95%;
        &__main {
          padding-bottom: 20px;
          color: var(--dark-main-color);
          font-size: 22px;
          font-weight: 500;
        }
        &__secondary {
          color: var(--lighter-text-color);
          font-size: 18px;
          font-weight: 300;
        }
      }
    }
  }
</style>
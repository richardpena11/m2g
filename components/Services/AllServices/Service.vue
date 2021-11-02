<template>
  <div>
    <div class="service">
      <div class="service__img">
        <img :src="require(`~/assets/${service.svg}`)" alt="">
      </div>
      <div class="service__title">
        {{ service.title }}
      </div>
      <div class="service__desc">
        {{ service.desc }}
      </div>
      <v-btn dark class="service__btn" :href="`#${service.anchor}`">
        Mas informacion
      </v-btn>
    </div>
  </div>
</template>

<script>
  export default {
    props: ["service"]
  }
</script>

<style lang="scss" scoped>
  .service {
    width: 250px;
    margin-bottom: 25px;
    display: flex;
    flex-direction: column;
    align-items: center;
    &__img {
      padding-bottom: 10px;
      width: 64px;
    }
    &__title {
      font-size: 18px;
      padding: 10px 0;
      color: var(--dark-main-color);
    }
    &__desc {
      text-align: center;
      font-weight: 300;
      color: var(--lighter-text-color);
    }
    &__btn {
      margin: 15px 0;
      background: var(--dark-main-color) !important;
    }
  }

  @media screen and (max-width: 1050px) {
    .service {
      width: 350px;
      &__desc {
        width: 250px;
      }
    }
  }

  @media screen and (max-width: 800px) {
    .service {
      width: 250px;
      &__desc {
        width: 250px;
      }
    }
  }
</style>
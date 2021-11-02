<template>
  <div class="all-reviews">
    <div id="reviews" class="anchor"></div>
    <div class="all-reviews__title">
      <h3 class="all-reviews__title__main">
        Nuestro Equipo
      </h3>
      <h3 class="all-reviews__title__desc">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sapien quam quam in tempus porttitor. Malesuada et purus facilisi at facilisis id nascetur laoreet non. Ac id congue aliquet ut risus in amet ac.
      </h3>
    </div>
    <div class="all-reviews__review">
      <Review v-for="(review, index) in 2" :key="index" />
    </div>
  </div>
</template>

<script>
import Review from './Review.vue'
  export default {
    components: { Review },
  }
</script>

<style lang="scss" scoped>
  .all-reviews {
    max-width: 1200px;
    width: 90%;
    margin: 0 auto;
    padding: 50px 0;
    &__title {
      text-align: center;
      margin-bottom: 75px; 
      &__main {
        padding-bottom: 20px;
        color: var(--dark-main-color);
        font-size: 26px;
        font-weight: 500;
      }
      &__desc {
        color: var(--lighter-text-color);
        font-size: 20px;
        font-weight: 300;
        line-height: 30px;
      }
    }
    &__review {
      display:  flex;
      justify-content: space-around;
      flex-wrap: wrap;
    }
  }

@media screen and (max-width: 800px) {
  .all-reviews {
    &__title {
      &__main {
        font-size: 22px;
      }
      &__desc {
        font-size: 18px;
      }
    }
  }
}
</style>
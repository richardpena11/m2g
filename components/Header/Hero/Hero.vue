<template>
  <div class="hero">
    <div class="hero__logo">
      <img class="hero__logo__svg" src="~assets/MergeToGrowWhite.svg" alt="M2G Logo">
    </div>
    <div class="hero__title">
      <h2 class="hero__title__main">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam augue.
      </h2>
      <h3 class="hero__title__secondary">
        Lorem ipsum dolor sit amet, consectetur adipiscing
      </h3>
    </div>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>
  .hero {
    height: 400px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    &__logo {
      &__svg {
        width: 350px;
      }
    }
    &__title {
      width: 550px;
      color: var(--white-color);
      &__main, &__secondary {
        margin: 20px 0;
      }
      &__main {
        font-weight: 500;
        font-size: 26px;

      }
      &__secondary {
        font-weight: 400;
        font-size: 22px;
      }
    }
  }
  @media screen and (max-width: 1100px) {
    .hero {
      margin-top: 50px;
      height: initial;
      flex-direction: column;
      &__logo {
        &__svg {
          width: 300px;
          margin-bottom: 25px;
        }
      }
      &__title {
        width: 95%;
        max-width: 600px;
        &__main {
          font-size: 22px;

        }
        &__secondary {
          font-size: 20px;
        }
      }
    }
  }
</style>
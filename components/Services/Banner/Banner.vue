<template>
  <div class="banner">
    <h5 class="banner__text">¿Estas buscando como contactarnos? Puedes hacerlo aqui</h5>
    <v-btn href="#contact" class="banner__btn">Contactanos</v-btn>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>
  .banner {
    position: absolute;
    height: 150px;
    right: 0;
    width: 100vw;
    background: var(--bg-gradient-color);
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
    &__text {
      width: 90%;
      text-align: center;
      font-size: 20px;
      color: var(--white-color);
    }
    &__btn {
      color: var(--dark-main-color);
    }
  }
</style>
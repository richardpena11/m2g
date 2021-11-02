<template>
  <div class="header_container">
    <div id="header" class="anchor"></div>
    <header class="header">
      <Nav />
      <Hero />
    </header>
    <!-- <img class="header-bg" src="~assets/HeaderBG.svg" alt="" /> -->
  </div>
</template>

<script>
import Nav from './Nav/Nav.vue'
import Hero from './Hero/Hero.vue'
export default {
  components: {
    Nav,
    Hero,
  },
}
</script>

<style lang="scss">
.header_container {
  display: flex;
  align-content: center;
  width: 100%;
  height: 500px;
  background: var(--bg-gradient-color);
  .header {
    width: 90%;
    max-width: 1200px;
    margin-top: 64px;
    position: absolute;
    left: 0; 
    right: 0; 
    margin-left: auto; 
    margin-right: auto; 
    z-index: 2;
    .v-sheet {
      margin: 0 auto;
    }
    .v-app-bar--is-scrolled {
      background: var(--bg-gradient-color) !important;
    }
  }
  .header-bg {
    color: #000;
    min-width: 1440px;
    width: 100vw;
    height: 590px;
    margin: 0 auto;
    top: 0;
    z-index: 1;
  }
}
</style>

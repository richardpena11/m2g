<template>
  <v-app>
    <Header />
    <Services />
    <Team />
    <Contact />
    <Reviews />
    <Footer />
  </v-app>
</template>

<script></script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,300;0,400;0,500;0,700;1,300&display=swap');

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Roboto', sans-serif;
  }

  :root {
    --black-color: #162927;
    --lighter-text-color: #394947;
    --dark-main-color: #2A7A71;
    --dark-main-color-rgb: 42, 122, 113;
    --main-color: #3BB0A8;
    --light-main-color: #D5F2F0;
    --light-main-color-rgb: 213, 242, 240;
    --white-color: #FFFFFF;
    --bg-gradient-color: linear-gradient(270deg, #3bb0a8 0%, #2a7a71 100%);
  }

  html {
    scroll-behavior: smooth;
  }

  .container {
    width: 1200px;
  }

  div.anchor {
    position: relative;
    top: -100px;
    visibility: hidden;
  }
</style>


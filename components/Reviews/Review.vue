<template>
  <div class="review">
    <span class="review__name">
      John Doe
    </span>
    <div class="review__info">
      “ Lorem ipsum dolor sit amet, consectetur adipiscing elit. Viverra tortor amet sed velit dapibus laoreet. Eget in scelerisque arcu eget egestas nulla. Ut fermentum pharetra sed aliquam laoreet vulputate cras amet sed. Lectus nulla ultrices luctus aliquet nunc vel. ”
    </div>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>
  .review {
    position: relative;
    width: 515px;
    padding: 30px 25px;
    border-radius: 24px;
    background: rgba(var(--light-main-color-rgb), .5);
    margin-bottom: 30px;
    &::before {
      content: '“';
      position: absolute;
      color: rgba(var(--dark-main-color-rgb), .08);
      -webkit-text-stroke: 1px rgba(var(--dark-main-color-rgb), .15);
      font-family: 'Roboto', sans-serif;
      font-size: 128px;
    }
    &::after {
      content: '”';
      position: absolute;
      right: 20px;
      bottom: 25px;
      color: rgba(var(--dark-main-color-rgb), .08);
      -webkit-text-stroke: 1px rgba(var(--dark-main-color-rgb), .15);
      font-family: 'Roboto', sans-serif;
      font-size: 128px;
      line-height: 0px;
    }
    &__name {
      margin-bottom: 15px;
      font-weight: 500;
      display: block;
    }
    &__info {
      margin-bottom: 15px;
      line-height: 22px;
      font-weight: 300;
      font-style: italic;
    }
  }
</style>
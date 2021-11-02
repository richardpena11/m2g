<template>
  <div class="team-member">
    <div class="team-member__img"></div>
    <div class="team-member__title">
      <div class="team-member__title__name">Richard J. Pena</div>
      <div class="team-member__title__position">Web Developer</div>
    </div>
    <div class="team-member__desc">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cursus nisi faucibus eleifend odio pellente. Nulla arcu enim, ultrices vestibulum vitae dignissim egestas lectus in.</div>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>
  .team-member {
    width: 250px;
    display: flex;
    flex-direction: column;
    align-items: center;
    &__img {
      width: 250px;
      height: 250px;
      margin-bottom: 20px;
      border-radius: 24px;
      background: #ccc;
    }
    &__title {
      text-align: center;
      &__name {
        font-size: 20px;
        font-weight: 500;
      }
      &__position {
        padding: 10px 0;
        font-size: 18px;
        color: var(--dark-main-color);
      }
    }
    &__desc {
      margin-top: 5px;
      line-height: 22px;
      font-weight: 300;
      color: var(--lighter-text-color);
    }
  }

  @media screen and (max-width: 900px) {
    .team-member {
      width: 300px;
      margin-bottom: 30px;
      &__desc {
        width: 250px;
      }
    }
  }
</style>
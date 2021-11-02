<template>
  <div :class="`all-detailed-services-container ${index % 2 == 0 ? '' : 'all-detailed-services-container--bg'}`">
    <div :id="service" class="anchor"></div>
    <div class="all-detailed-services">
      <div class="all-detailed-services__info">
        <div class="all-detailed-services__info__title">Websites</div>
        <div class="all-detailed-services__info__desc">
          <div class="all-detailed-services__info__desc__bullet">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc purus lectus, mollis eget ipsum sed, pretium sagittis metus. Morbi pellentesque nisi non magna aliquet
          </div>
          <div class="all-detailed-services__info__desc__bullet">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc purus lectus, mollis eget ipsum sed, pretium sagittis metus. Morbi pellentesque nisi non magna aliquet
          </div>
          <div class="all-detailed-services__info__desc__bullet">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc purus lectus, mollis eget ipsum sed, pretium sagittis metus. Morbi pellentesque nisi non magna aliquet
          </div>
        </div>
      </div>
      <div class="all-detailed-services__img">
        <div class="all-detailed-services__img__svg"></div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: ["index", "service"]
  }
</script>

<style lang="scss" scoped>
  .all-detailed-services-container {
    .all-detailed-services {
      width: 95%;
      max-width: 1000px;
      margin: 0 auto;
      padding: 50px 0;
      display: flex;
      flex-direction: row;
      justify-content: space-around;
      align-items: center;
      &__info {
        width: 60%;
        &__title {
          display: block;
          position: relative;
          font-weight: 500;
          font-size: 26px;
          &::after {
            content: '';
            display: block;
            margin: 5px 0;
            width: 45px;
            height: 4px;
            background: var(--dark-main-color);
          }
        }
        &__desc {
          font-weight: 300;
          line-height: 24px;
          color: var(--lighter-text-color);
          &__bullet {
            padding: 20px 0;
          }
        }
      }
      &__img {
        display: flex;
        justify-content: flex-end;
        &__svg {
          width: 350px;
          height: 350px;
          background: #ccc;
        }
      }
    }
    &--bg {
      position: relative;
      width: 100vw;
      background: var(--light-main-color);
      .all-detailed-services {
        flex-direction: row-reverse;
        &__img {
          justify-content: flex-start;
        }
      }
    }
  }
  @media screen and (max-width: 1000px) {
    .all-detailed-services-container { 
      .all-detailed-services {
        &__info {
          width: 50%;
        }
      }
    }
  }

  @media screen and (max-width: 820px) {
    .all-detailed-services-container { 
      .all-detailed-services {
        flex-direction: column;
        &__info {
          width: 95%;
        }
      }
    }
  }
</style>
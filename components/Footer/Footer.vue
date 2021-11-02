<template>
  <div class="footer-container">
    <div class="footer">
      <div class="footer__info">
        <div class="footer__info__logo">
          <img
            class="footer__info__logo__svg"
            src="~assets/MergeToGrowWhite.svg"
            alt="M2G Logo"
          />
        </div>
        <div class="footer__info__desc">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nec
          sagittis dui. In erat felis, ornare fermentum finibus a, aliquam ut
          mauris. Curabitur sit amet neque varius, volutpat nisi vitae, gravida
          metus. Ut aliquet urna enim, in ullamcorper tortor suscipit lacinia.
          Curabitur in ante consectetur, feugiat enim facilisis, tincidunt
          nulla.
        </div>
      </div>
      <div class="footer__sitemap">
        <div class="footer__sitemap__section">
          <div class="footer__sitemap__section__title">Servicios</div>
          <ul class="footer__sitemap__section__list">
            <li><a href="#website">Desarrollo Web</a></li>
            <li><a href="#taxes">Impuestos</a></li>
            <li><a href="#finances">Finanzas</a></li>
            <li><a href="#insurance">Seguros</a></li>
          </ul>
        </div>
        <div class="footer__sitemap__section">
          <div class="footer__sitemap__section__title">Enlaces</div>
          <ul class="footer__sitemap__section__list">
            <li><a href="#header">Inicio</a></li>
            <li><a href="#services">Servicios</a></li>
            <li><a href="#team">Equipo</a></li>
            <li><a href="#contact">Contacto</a></li>
            <li><a href="#reviews">Reseña</a></li>
          </ul>
        </div>
        <div class="footer__sitemap__section footer__sitemap__contact">
          <div class="footer__sitemap__section__title">Contacto</div>
          <ul class="footer__sitemap__section__list">
            <li>Davenport, FL</li>
            <li>admin@mergetogrow.com</li>
            <li>+1 (000) 000 0000</li>
          </ul>
          <div
            class="
              footer__sitemap__section__social footer__sitemap__contact__social
            "
          >
            <v-icon> mdi-facebook </v-icon>
            <v-icon> mdi-instagram </v-icon>
            <v-icon> mdi-twitter </v-icon>
          </div>
        </div>
      </div>
      <div class="footer__copyright">
        <div class="footer__copyright__line"></div>
        <div class="footer__copyright__text">
          ©2021 copyright all right reserved by Merge To Grow
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.footer-container {
  padding-top: 50px;
  padding-bottom: 30px;
  color: var(--white-color);
  background: var(--black-color);
  .footer {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    &__info {
      display: flex;
      flex-direction: column;
      align-items: center;
      max-width: 450px;
      width: 30%;
      &__logo {
        width: 150px;
        margin-bottom: 25px;
      }
      &__desc {
        color: rgba(var(--light-main-color-rgb), 0.75);
      }
    }
    &__sitemap {
      max-width: 600px;
      width: 70%;
      height: 100%;
      display: flex;
      justify-content: space-between;
      &__section {
        &__title {
          margin-bottom: 15px;
        }
        &__list {
          padding-left: 0;
          list-style: none;
          li {
            padding: 5px 0;
            color: rgba(var(--light-main-color-rgb), 0.75);
            &:hover {
              color: var(--white-color);
            }
            a {
              color: rgba(var(--light-main-color-rgb), 0.75);
              text-decoration: none;
            }
          }
        }
      }
      &__contact {
        display: flex;
        flex-direction: column;
        &__social {
          margin-top: auto;
          align-self: flex-end;
          .v-icon {
            padding: 0 5px;
            font-size: 28px;
            color: rgba(var(--light-main-color-rgb), 0.75);
            cursor: pointer;
            &:hover {
              color: var(--white-color);
            }
          }
        }
      }
    }
    &__copyright {
      width: 100%;
      &__line {
        margin-top: 50px;
        height: 2px;
        width: 100%;
        background: rgba(var(--light-main-color-rgb), 0.75);
      }
      &__text {
        margin-top: 20px;
        text-align: center;
        color: rgba(var(--light-main-color-rgb), 0.75);
      }
    }
  }
}

@media screen and (max-width: 1000px) {
  .footer-container {
    .footer {
      &__info {
        max-width: initial;
        width: 100%;
        margin-bottom: 30px;
      }
      &__sitemap {
        max-width: initial;
        width: 100%;
      }
    }
  }
}
</style>

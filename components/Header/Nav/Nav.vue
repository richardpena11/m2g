<template>
  <v-app-bar color="transparent" fixed elevate-on-scroll>
    <nav class="nav">
      <div class="nav__business">
        <div class="nav__business__logo">
          <img
            class="nav__business__logo__svg"
            src="~assets/M2GWhite.svg"
            alt="M2G Logo"
          />
        </div>
        <div class="nav__business__info">
          <v-btn class="nav__business__info__btn">
            <a href="#contact">Contactanos</a>
          </v-btn>
        </div>
      </div>
      <ul class="nav__links">
        <li class="nav__links__link">
          <a href="#header">Inicio</a>
        </li>
        <li class="nav__links__link">
          <a href="#services">Servicios</a>
        </li>
        <li class="nav__links__link">
          <a href="#team">Equipo</a>
        </li>
        <li class="nav__links__link">
          <a href="#contact">Contacto</a>
        </li>
        <li class="nav__links__link">
          <a href="#reviews">Reseña</a>
        </li>
      </ul>

      <v-menu class="nav__burger" bottom left>
        <template v-slot:activator="{ on, attrs }">
          <v-btn dark icon v-bind="attrs" v-on="on">
            <v-icon>mdi-menu</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item class="nav__links__link nav__links__link--responsive">
            <v-list-item-title>
              <a href="#header">Inicio</a>
            </v-list-item-title>
          </v-list-item>

          <v-list-item class="nav__links__link nav__links__link--responsive">
            <v-list-item-title>
              <a href="#services">Servicios</a>
            </v-list-item-title>
          </v-list-item>

          <v-list-item class="nav__links__link nav__links__link--responsive">
            <v-list-item-title>
              <a href="#team">Equipo</a>
            </v-list-item-title>
          </v-list-item>

          <v-list-item class="nav__links__link nav__links__link--responsive">
            <v-list-item-title>
              <a href="#contact">Contacto</a>
            </v-list-item-title>
          </v-list-item>

          <v-list-item class="nav__links__link nav__links__link--responsive">
            <v-list-item-title>
              <a href="#reviews">Reseña</a>
            </v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </nav>
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {}
  },
}
</script>

<style lang="scss">
.nav {
  margin: 0 auto;
  width: 1200px;
  padding: 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  &__business {
    width: 220px;
    display: flex;
    justify-content: space-between;
    &__logo {
      margin-right: 20px;
      &__svg {
        width: 80px;
      }
    }
    &__info {
      display: flex;
      font-size: 18px;
      &__btn {
        a {
          color: var(--dark-main-color);
          text-decoration: none;
        }
      }
    }
  }
  &__links {
    display: flex;
    list-style: none;
    &__link {
      a {
        padding: 10px 15px;
        text-decoration: none;
        font-size: 18px;
        font-weight: 300;
        color: var(--white-color);
        border-bottom: 3px solid transparent;
        transition: border 200ms;
        &:hover {
          border-bottom: 3px solid var(--white-color);
        }
      }
      &--responsive {
        .v-list-item__title {
          a {
            font-weight: 400;
            color: var(--dark-main-color);
          }
        }
      }
    }
  }
  > .v-btn {
    display: none;
    .v-btn__content {
      .v-icon {
        font-size: 32px;
      }
    }
  }
}

@media screen and (max-width:800px) {
  .nav {
    &__links {
      display: none;
    }
    > .v-btn {
      display: initial;
    }
  }
}
</style>

<template>
  <div class="contact-container">
    <div id="contact" class="anchor"></div>
    <div class="contact">
      <div class="contact__title">
        <h3 class="contact__title__main">Contactanos</h3>
        <h3 class="contact__title__desc">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam et
          purus et purus varius vestibulum. Phasellus finibus nulla tortor, ut
          ullamcorper diam porta sit amet. Integer congue laoreet felis.
        </h3>
      </div>
      <div class="contact__info">
        <form class="contact__info__form">
          <v-text-field
            v-model="formData.name"
            class="contact__info__form__name contact__info__form__input"
            :rules="[rules.required]"
            label="Tu Nombre"
            color="#3BB0A8"
          ></v-text-field>
          <v-text-field
            v-model="formData.email"
            class="contact__info__form__email contact__info__form__input"
            :rules="[rules.required, rules.email]"
            label="Tu Email"
            color="#3BB0A8"
          ></v-text-field>
          <v-select
            v-model="formData.service"
            class="contact__info__form__service contact__info__form__input"
            :items="items"
            :rules="[rules.required]"
            :menu-props="{ offsetY: true }"
            label="Servicio a consultar"
            color="#3BB0A8"
          ></v-select>
          <v-text-field
            v-model="formData.title"
            class="contact__info__form__subject contact__info__form__input"
            :rules="[rules.required]"
            label="Titulo"
            color="#3BB0A8"
          ></v-text-field>
          <v-textarea
            v-model="formData.message"
            class="contact__info__form__message contact__info__form__input"
            :rules="[rules.required]"
            label="Tu Mensaje"
            color="#3BB0A8"
          ></v-textarea>
          <v-btn @click="sendForm" class="contact__info__form__btn"
            >Enviar</v-btn
          >
        </form>
        <div class="contact__info__social">
          <div class="contact__info__social__icon">
            <v-icon> mdi-facebook </v-icon>
            <span class="contact__info__social__icon__name"> MergeToGrow </span>
          </div>
          <div class="contact__info__social__icon">
            <v-icon>mdi-instagram</v-icon>
            <span class="contact__info__social__icon__name">
              @MergeToGrow
            </span>
          </div>
          <div class="contact__info__social__icon">
            <v-icon>mdi-twitter</v-icon>
            <span class="contact__info__social__icon__name">
              @MergeToGrow
            </span>
          </div>
        </div>
        <div class="contact__info__extra">
          <div class="contact__info__extra__service">
            <div class="contact__info__extra__service__title">Website</div>
            <div class="contact__info__extra__service__info">
              <span>Web@mergetogrow.com</span>
              <span>+1 (407) 755-9648</span>
            </div>
          </div>
          <div class="contact__info__extra__service">
            <div class="contact__info__extra__service__title">
              Taxes and Finances
            </div>
            <div class="contact__info__extra__service__info">
              <span>taxes@mergetogrow.com</span>
              <span>finances@mergetogrow.com</span>
              <span>+1 (407) 755-9648</span>
            </div>
          </div>
          <div class="contact__info__extra__service">
            <div class="contact__info__extra__service__title">Website</div>
            <div class="contact__info__extra__service__info">
              <span>Web@mergetogrow.com</span>
              <span>+1 (407) 755-9648</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
/* eslint-disable no-console */
import emailjs from "emailjs-com";

export default {
  data() {
    return {
      formData: {
        name: 'Richard',
        email: 'v29590611@gmail.com',
        service: 'Impuestos',
        serviceEmail: '',
        title: 'Title',
        message: 'message',
      },
      emailID: {
        userID: 'user_5iEbYepf1b2zL2m4z4JJi',
        serviceID: 'service_m2g',
        templateID: 'template_m2g',
      },
      items: ['Impuestos', 'Paginas Web', 'Seguros', 'Finanzas'],
      emails: ['taxes@mergetogrow.com', 'web@mergetogrow.com', 'insurance@mergetogrow.com', 'finances@mergetogrow.com'],
      rules: {
        required: value => !!value || 'Este campo es requerido.',
        counter: value => value.length <= 100 || 'El mensaje tiene que ser menor a 100 caracteres',
        email: value => {
          const pattern = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
          return pattern.test(value) || 'Tiene que ser un Email valido.'
        },
      },
    }
  },

  methods: {
    sendForm(){
      const formData = this.formData;
      const emailID = this.emailID;

      const items = this.items
      const serviceIndex = items.findIndex(value => value === formData.service)
      this.formData.serviceEmail = this.emails[serviceIndex]

      let checkData = true;
      for (const item in formData) {
        if(formData[item] === '') {
          checkData = false
        }
      }

      if(checkData) {
        // eslint-disable-next-line import/no-named-as-default-member
        emailjs
          .send(emailID.serviceID, emailID.templateID, formData, emailID.userID)
          .then(function(response) {
            console.log('SUCCESS!', response.status, response.text);
          }, function(error) {
            console.log('FAILED...', error);
          });
      } else {
        console.log('No se envio')
      }
    }
  },
}
</script>

<style lang="scss" scoped>
.contact-container {
  padding: 50px 0;
  background: var(--bg-gradient-color);
  .contact {
    max-width: 1200px;
    width: 90%;
    margin: 0 auto;
    &__title {
      text-align: center;
      margin-bottom: 30px;
      &__main {
        padding-bottom: 20px;
        font-size: 26px;
        font-weight: 500;
        color: var(--white-color);
      }
      &__desc {
        font-size: 20px;
        font-weight: 300;
        line-height: 30px;
        color: var(--white-color);
      }
    }
    &__info {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      align-items: center;
      padding: 25px 50px;
      border-radius: 24px;
      background: var(--white-color);
      &__form {
        display: flex;
        flex-wrap: wrap;
        width: 55%;
        &__input {
          width: 100%;
        }
        &__name,
        &__email {
          width: 40%;
        }
        &__name {
          margin-right: 50px;
        }
        &__service {
          .v-input__control {
            .v-input__slot {
              .v-menu {
                display: initial !important;
              }
            }
          }
        }
        &__btn {
          margin: 10px auto 0 auto;
          background: var(--main-color);
          color: var(--white-color);
        }
      }
      &__social {
        &__icon {
          display: flex;
          flex-direction: column;
          align-items: center;
          padding: 10px 0;
          .v-icon {
            padding: 10px 0;
            color: var(--dark-main-color);
            font-size: 56px;
          }
        }
      }
      &__extra {
        display: flex;
        flex-direction: column;
        &__service {
          padding: 10px 0;
          text-align: center;
          &__title {
            padding: 10px;
            font-size: 22px;
            font-weight: 500;
          }
          &__info {
            display: flex;
            flex-direction: column;
            span {
              padding: 5px 0;
              font-weight: 300;
              color: var(--lighter-text-color);
            }
          }
        }
      }
    }
  }
}

@media screen and (max-width: 1000px) {
  .contact-container {
    .contact {
      &__info {
        &__form {
          width: 100%;
          margin-bottom: 30px;
        }
        &__social {
          width: 100%;
          display: flex;
          justify-content: space-evenly;
        }
        &__extra {
          width: 100%;
          flex-direction: row;
          justify-content: space-evenly;
        }
      }
    }
  }
}

@media screen and (max-width: 800px) {
  .contact-container {
    .contact {
      &__title {
        &__main {
          font-size: 22px;
        }
        &__desc {
          font-size: 18px;
        }
      }
      &__info {
        padding: 20px 30px;
        &__social {
          justify-content: space-around;
          &__icon {
            .v-icon {
              font-size: 56px;
            }
          }
        }
        &__extra {
          justify-content: space-between;
          &__service {
            &__title {
              font-size: 20px;
            }
            &__info {
              span {
                font-size: 14px;
              }
            }
          }
        }
      }
    }
  }
}

@media screen and (max-width: 650px) {
  .contact-container {
    .contact {
      &__info {
        &__social {
          width: 40%;
          flex-direction: column;
        }
        &__extra {
          width: 60%;
          flex-direction: column;
        }
      }
    }
  }
}
</style>

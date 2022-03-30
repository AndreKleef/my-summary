<template>
  <footer class="footer">
    <div class="footer__container container">
      <div class="footer__main">
        <router-link class="footer__logo" to="/">
          <img class="footer__logo-pic" alt="logo" v-bind:src="logoWhite">
        </router-link>
        <ul class="footer__list">
          <li class="footer__item">
            <a class="footer__social" target="_blank" href="tel:89915127645">
              <span class="footer__social-icon footer__social-icon_phone"></span>
              <span class="footer__social-link text" >8 991 512 76 45</span>
            </a>
          </li>
          <li class="footer__item">
            <a class="footer__social" target="_blank" href="mailto:kleef001@gmail.com">
              <span class="footer__social-icon footer__social-icon_mail"></span>
              <span class="footer__social-link text" >kleef001@gmail.com</span>
            </a>
          </li>
          <li class="footer__item">
            <a class="footer__social" target="_blank" href="https://t.me/AndreSlivka">
              <span class="footer__social-icon footer__social-icon_telegram"></span>
              <span class="footer__social-link text" >@AndreSlivka</span>
            </a>
          </li>
        </ul>
      </div>
      <span class="footer-text text" v-show="date">{{ date }}</span>
    </div>
  </footer>
</template>

<script>
  import logoWhite from '../assets/img/logo_white.png';

  export default {
    name: 'myFooter',
    data() {
      return {
        date: '',
        logoWhite: logoWhite
      }
    },
    methods: {
      printDate: function () {
        return new Date().toLocaleDateString();
      }
    },
    mounted: function () {
      this.date = this.printDate();
    }
  }
</script>

<style scoped lang="scss">
  .footer {
    background: rgba(0,0,0,0.9);
    padding: 10px 0;
    min-height: 135px;

    @media (max-width: 575px) {
      padding: 20px 0;
    }

    &__container {
      display: flex;
      flex-direction: column;

      @media (max-width: 575px) {
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-start;
      }
    }

    &__logo {
      width: 300px;
      height: auto;
      padding: 6px 0;

      @media (max-width: 575px) {
        width: 240px;
      }

      &-pic {
        width: 100%;
        height: 100%;
      }
    }

    &__main {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;

      @media (max-width: 575px) {
        flex-direction: column;
      }
    }

    &-text {
      font-size: 14px;
      color: #676767;
    }

    &__list {
      @media (max-width: 575px) {
        margin: 10px 0;
      }
    }

    &__social {
      display: flex;
      align-items: center;
      justify-content: flex-start;
      padding: 6px 0;

      &-icon {
        background-position: center;
        background-size: contain;
        background-repeat: no-repeat;
        display: block;
        width: 24px;
        height: 24px;
        margin-right: 8px;


        &_phone {
          background-image: url('../assets/img/phone.svg');
        }
        &_mail {
          background-image: url('../assets/img/mail.svg');
        }
        &_telegram {
          background-image: url('../assets/img/tg.svg');
        }
      }

      &-link {
        color: #ffffff;
        font-size: 16px;
        transition: 0.2s;

        &:hover {
          color: #676767;
        }
      }
    }
  }
</style>

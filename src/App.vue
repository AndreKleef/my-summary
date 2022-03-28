<template>
  <header class="page-header">
    <div class="page-header__container container">
      <router-link class="page-header__logo" to="/">
        <img class="page-header__logo-pic" alt="logo" src="./assets/img/logo_black.png">
      </router-link>
      <nav class="page-header__nav" :class="{ active_nav: active }">
        <router-link class="page-header__nav-link" to="/">Главная</router-link>
        <router-link class="page-header__nav-link" to="/map">Геопозиция</router-link>
      </nav>
      <div class="burger" :class="{ active_burger: active }" id="burger" @click="active = !active" :aria-pressed="active ? 'true' : 'false'">
        <span class="burger-global burger-top"></span>
        <span class="burger-global burger-middle"></span>
        <span class="burger-global burger-bottom"></span>
      </div>
    </div>
  </header>

  <router-view/>

  <footer class="page-footer">
    <div class="page-footer__container container">
      <div class="page-footer__main">
        <router-link class="page-footer__logo" to="/">
          <img class="page-footer__logo-pic" alt="logo" src="./assets/img/logo_white.png">
        </router-link>
        <ul class="page-footer__list">
          <li class="page-footer__item">
            <a class="page-footer__social" target="_blank" href="tel:89915127645">
              <span class="page-footer__social-icon page-footer__social-icon_phone"></span>
              <span class="page-footer__social-link text" >8 991 512 76 45</span>
            </a>
          </li>
          <li class="page-footer__item">
            <a class="page-footer__social" target="_blank" href="mailto:kleef001@gmail.com">
              <span class="page-footer__social-icon page-footer__social-icon_mail"></span>
              <span class="page-footer__social-link text" >kleef001@gmail.com</span>
            </a>
          </li>
          <li class="page-footer__item">
            <a class="page-footer__social" target="_blank" href="https://t.me/AndreSlivka">
              <span class="page-footer__social-icon page-footer__social-icon_telegram"></span>
              <span class="page-footer__social-link text" >@AndreSlivka</span>
            </a>
          </li>
        </ul>
      </div>
      <span class="page-footer__main-text text">28.03.2022</span>
    </div>
  </footer>
</template>

<script>
  export default {
    data() {
      return {
        active: false
      }
    }
  }
</script>

<style lang="scss">

  * {
    font-family: 'Roboto', sans-serif;
    margin: 0;
    padding: 0;
    text-decoration: none;
    -webkit-tap-highlight-color:transparent;
  }

  ul,ol,li {
    list-style-type: none;
  }

  body {
    background: #f0f1f2;
  }

  .title {
    font-size: 36px;
    padding-bottom: 16px;
    letter-spacing: 1.5px;
    color: rgba(0,0,0,0.8);

    @media (max-width: 768px) {
      font-size: 28px;
    }
  }

  .subtitle {
    font-size: 30px;
    padding-bottom: 20px;
    letter-spacing: 1.5px;
    color: rgba(0,0,0,0.8);
    text-align: center;

    @media (max-width: 768px) {
      font-size: 24px;
    }
  }

  .text {
    font-size: 18px;
    line-height: 1.6;
    color: rgba(0,0,0,0.8);

    @media (max-width: 768px) {
      font-size: 14px;
    }
  }

  #app {
    .container {
      max-width: 1170px;
      padding: 0 15px;
      margin: 0 auto;
    }
  }

  .page-header {
    padding: 10px 0;
    width: 100%;
    height: 45px;
    position: sticky;
    top: 0;
    left: 0;
    background: #ffffff;
    z-index: 5;

    &__container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    &__logo {
      width: 300px;
      height: auto;

      @media (max-width: 575px) {
        width: 240px;
      }

      &-pic {
        width: 100%;
        height: 100%;
      }
    }

    &__nav {
      @media (max-width: 768px) {
        opacity: 0;
        visibility: hidden;
        background: #fff;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        padding: 20px 0px;
        display: flex;
        flex-direction: column;
        box-shadow: 0 2px 8px 0 rgb(0 0 0 / 20%);
        transition: 0.2s;
        &.active_nav {
          opacity: 1;
          visibility: visible;
          transition: 0.2s;

          & .page-header__nav-link {
            padding: 8px;
          }
        }
      }
      &-link {
        margin-left: 20px;
        color: #676767;
        letter-spacing: 1.1px;
        text-transform: uppercase;
        transition: 0.2s;
        font-size: 14px;

        &:hover {
          color: rgba(0,0,0,1);
        }
      }
    }
  }

  .burger {
    display: none;

    @media (max-width: 768px) {
      cursor: pointer;
      display: inline-block;
      width: 26px;
      height: 22px;
      transition: 0.4s;
      position: absolute;
      top: 50%;
      right: 15px;
      transform: translate(0, -50%);

      &-global {
        backface-visibility: hidden;
        position: absolute;
        border-top: 3px solid #777;
        border-radius: 10px;
        width: 100%;
        transition: 0.4s ease-out;
      }

      &-top {
        top: 0px;
        left: 0;
      }

      &-middle {
        top: 7px;
        left: 0;
      }

      &-bottom {
        top: 14px;
        left: 0;
      }

      &.active_burger {
        width: 26px;
        height: 22px;
        transition: all 0.4s ease;
        z-index: 1000;

        & .burger {
          &-top {
            transform: rotate(-225deg);
            top: 6px;
            border-top: 3px solid #777;
          }

          &-middle {
            opacity: 0;
          }

          &-bottom {
            transform: rotate(225deg);
            top: 6px;
            border-top: 3px solid #777;
          }
        }
      }
    }
  }

  .page-footer {
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

      &-text {
        font-size: 14px;
        color: #676767;
      }
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
          background-image: url('./assets/img/phone.svg');
        }
        &_mail {
          background-image: url('./assets/img/mail.svg');
        }
        &_telegram {
          background-image: url('./assets/img/tg.svg');
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

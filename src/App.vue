<template>
  <header class="page-header">
    <div class="page-header__container container">
      <div class="page-header__image">
        <img class="page-header__image-pic" alt="logo" src="./assets/img/logo_black.png">
      </div>
      <nav class="page-header__nav">
        <router-link class="page-header__nav-link" to="/">Главная</router-link>
        <router-link class="page-header__nav-link" to="/map">Геопозиция</router-link>
      </nav>
    </div>
  </header>

  <router-view/>

  <footer class="page-footer">
    <div class="page-footer__container container">
      <div class="page-footer__main">
        <div class="page-footer__image">
          <img class="page-footer__image-pic" alt="logo" src="./assets/img/logo_white.png">
        </div>
        <span class="page-footer__main-text text">29.03.2022</span>
      </div>

      <ul class="page-footer__list">
        <li class="page-footer__item">
          <a class="page-footer__social" target="_blank" href="tel:84938493832">
            <span class="page-footer__social-icon page-footer__social-icon_phone"></span>
            <span class="page-footer__social-link text" >8 991 512 76 45</span>
          </a>
        </li>
        <li class="page-footer__item">
          <a class="page-footer__social" target="_blank" href="mailto:84938493832">
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
  </footer>
</template>

<script>

</script>

<style lang="scss">


* {
  font-family: 'Roboto', sans-serif;
  margin: 0;
  padding: 0;
  text-decoration: none;
}

ul,ol,li {
  list-style-type: none;
}

body {
  background: #f0f1f2;
}

.title {
  font-size: 36px;
  padding-bottom: 24px;
  letter-spacing: 1.5px;
  color: rgba(0,0,0,0.8);
}

.subtitle {
  font-size: 30px;
  padding-bottom: 20px;
  letter-spacing: 1.5px;
  color: rgba(0,0,0,0.8);
  text-align: center;
}

.text {
  font-size: 18px;
  line-height: 1.6;
  color: rgba(0,0,0,0.8);
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

  &__image {
    width: 300px;
    height: auto;

    &-pic {
      width: 100%;
      height: 100%;
    }
  }

  &__nav {
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

.page-footer {
  background: rgba(0,0,0,0.9);
  padding: 10px 0;

  &__container {
    display: flex;
    justify-content: space-between;
  }

  &__main {
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    &-text {
      font-size: 14px;
      color: #676767;
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

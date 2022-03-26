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
    <ul class="page-footer__list">
      <li class="page-footer__item">
        <a class="page-footer__item-link" href="tel:84938493832">8 932 213 12 23</a>
      </li>
      <li class="page-footer__item">
        <a class="page-footer__item-link" href="tel:84938493832">8 932 213 12 23</a>
      </li>
    </ul>
  </footer>
</template>

<style lang="scss">


* {
  font-family: 'Roboto', sans-serif;
  margin: 0;
  padding: 0;
  text-decoration: none;
}

.title {
  color: rgba(0,0,0,0.8);
}

.text {
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
}

</style>

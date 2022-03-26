<template>
  <header class="page-header">
    <nav>
      <router-link to="/">Главная</router-link> |
      <router-link to="/map">Геопозиция</router-link>
    </nav>
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
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>

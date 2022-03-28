<template>
  <div class="map__block">
    <div class="map__container container">
      <iframe id="map" src="https://yandex.ru/map-widget/v1/?um=constructor%3Ad32c137f06142281e8ad5423cd5a6cb2b9327148792a6e6d7b242d6a97f2ad48&amp;source=constructor" width="100%" height="800" frameborder="0"></iframe>
    </div>
  </div>
</template>


<script>
  export default {
    name: 'HelloWorld',
    props: {
      msg: String
    }
  }
</script>

<style lang="scss">
  #app .map {
    min-height: calc(100vh - 155px - 65px);

    &__container {
      @media (max-width: 768px) {
        padding: 0 25px;
      }
    }

    #map {
      @media (max-width: 768px) {
        height: 700px;
      }
      @media (max-width: 575px) {
        height: 500px;
      }
    }
  }
</style>

<template>
  <div class="promo">
    <div class="promo__container container">
      <div class="promo__content">
        <h1 class="promo__content-title title">{{ title }}</h1>
        <p class="promo__content-text text">
          На протяжении всего путешествия по мини сайту, вы узнаете, что я использую для реализации верстки и разработки,
          где набрался опыта, и что еще нужно освоить для того, чтобы комфортно себя чувствовать в сфере IT, конкретно Frontend, приятного вам пути! ;)
        </p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'mainPromo',
    props: {
      title: String
    }
  }
</script>

<style scoped lang="scss">

  .promo {
    background: url('../../assets/img/promo.jpeg') no-repeat center/cover;
    width: 100%;
    height: 600px;
    position: relative;

    @media (max-width: 768px) {
      height: 360px;
    }

    &::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.45);
      z-index: 1;
    }

    &::after {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 45%;
      height: 100%;
      background: rgba(238, 238, 238, 0.65);
      z-index: 1;

      @media (max-width: 768px) {
        width: 100%;
      }
    }

    &__container {
      position: relative;
      height: 100%;
    }

    &__content {
      position: absolute;
      top: 50%;
      transform: translate(0, -50%);
      left: 15px;
      width: 37%;
      z-index: 2;

      @media (max-width: 768px) {
        width: 75%;
      }
      @media (max-width: 575px) {
        width: 90%;
        padding: 0 15px;
        left: 0;
      }
    }
  }
</style>

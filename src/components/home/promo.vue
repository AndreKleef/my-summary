<template>
  <div class="promo">
    <div class="promo__container container">
      <div class="promo__content">
        <h1 class="promo__content-title title">{{ msg }}</h1>
        <p class="promo__content-text text">
          На протяжении всего путешествия по мини сайту, вы узнаете, что я умею,
          где набрался опыта, что могу использовать, а что в процессе обучения, приятного пути! ;)
        </p>
      </div>
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


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

  .promo {
    background: url('../../assets/img/promo.jpeg') no-repeat center/cover;
    width: 100%;
    height: 600px;
    position: relative;

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
    }
  }
</style>

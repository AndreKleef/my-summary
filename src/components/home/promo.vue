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
    background: url('../../assets/img/promo-2.jpeg') no-repeat center/cover;
    width: 100%;
    height: 700px;
    position: relative;

    &::after {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.45);
    }
  }
</style>

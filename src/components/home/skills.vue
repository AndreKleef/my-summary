<template>
  <div class="skills">
    <div class="skills__container container">
      <h2 class="skills-title subtitle">{{ msg }}</h2>
      <div class="skills__cards">
        <div class="skills__item" v-for="skills in column" :key="skills">
          <div class="skills__image">
            <img class="skills__image-pic" alt="skill" :src='skills.image'>
          </div>
          <p class="skills__item-text text">{{skills.title}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      column: [
        {
          image: require('../../assets/img/icon-html.png'),
          title: 'HTML — стандартизированный язык разметки документов для просмотра веб-страниц в браузере.',
        },
        {
          image: require('../../assets/img/icon-css.png'),
          title: 'CSS — стандартизированный язык разметки документов для просмотра веб-страниц в браузере.',
        },
        {
          image: require('../../assets/img/icon-js.png'),
          title: 'JS — стандартизированный язык разметки документов для просмотра веб-страниц в браузере.',
        },
        {
          image: require('../../assets/img/icon-github.png'),
          title: 'GIT — стандартизированный язык разметки документов для просмотра веб-страниц в браузере.',
        },
        {
          image: require('../../assets/img/icon-responsive.png'),
          title: 'RESPONSIVE — стандартизированный язык разметки документов для просмотра веб-страниц в браузере.',
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">

  .skills {
    margin: 60px 0 36px 0;

    @media (max-width: 1200px) {
      margin: 30px 0 0 0;
    }

    &__cards {
      display: flex;
      text-align: center;
      flex-wrap: wrap;
      padding: 20px 0;

      @media (max-width: 1200px) {
        flex-wrap: nowrap;
        overflow-x: auto;
      }
    }

    &__item {
      width: 182px;
      padding: 16px;
      margin-bottom: 24px;
      border-radius: 4px;
      background: #ffffff;
      transition: 0.2s;
      cursor: pointer;

      &-text {
        font-size: 16px;
      }

      &:not(:nth-child(5n + 5)) {
        margin-right: 24px;
      }

      &:hover {
        box-shadow: 0 2px 8px 0 rgb(0 0 0 / 20%);
      }

      @media (max-width: 1200px) {
        margin: 0 24px 0 0;
      }
    }

    &__image {
      width: 100px;
      height: 100px;
      margin: 0 auto 12px auto;

      &-pic {
        width: 100%;
        height: 100%;
      }
    }
  }
</style>

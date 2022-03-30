<template>
  <div class="skills">
    <div class="skills__container container">
      <h2 class="skills-title subtitle">{{ title }}</h2>
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
    name: 'mySkills',
    props: {
      title: String
    },
    data() {
      return {
        column: [
          {
            image: require('../../assets/img/icon-html.png'),
            title: 'HTML5 — Здесь практика и еще раз практика, поэтому в его освоении не было проблем, БЭМ в том числе, с Twig почти на "ТЫ"',
          },
          {
            image: require('../../assets/img/icon-css.png'),
            title: 'CSS3 — зачем нужен CSS, когда есть SCSS) структурно расположить стили, чтобы было красиво и без лишней перезаписи) mixins только пользовался, с нуля не писал, но проблем в этом не вижу',
          },
          {
            image: require('../../assets/img/icon-github.png'),
            title: 'GIT — в компании (где сейчас работаю) используем bitbucket, поэтому переход на github пробем не составит',
          },
          {
            image: require('../../assets/img/icon-js.png'),
            title: 'JS — здесь все серьезно! На данный момент изучаю основы, в компании и за его пределами, решаю не большие задачи',
          },
          {
            image: require('../../assets/img/icon-vue.png'),
            title: 'Vue.js — лично для меня он всегда был интересен, но не решался углубляться, поскольку знаний JS маловато, но при сборке этого сайта, так сказать... сегодня был небольшой толчок в развитии ;)',
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
      width: 190px;
      padding: 16px 12px;
      margin-bottom: 24px;
      border-radius: 4px;
      background: #ffffff;

      &-text {
        font-size: 14px;
      }

      &:not(:nth-child(5n + 5)) {
        margin-right: 25px;
      }

      @media (max-width: 1200px) {
        width: 100%;
        margin-bottom: 0;
        flex: 0 0 190px;

        &:not(:nth-child(5n + 5)) {
          margin-right: 0;
        }

        &:not(:last-of-type) {
          margin-right: 25px;
        }
      }
    }

    &__image {
      width: 100px;
      height: 100px;
      margin: 0 auto 12px;
      display: flex;
      align-items: center;

      &-pic {
        width: 100%;
        height: auto;
      }
    }
  }
</style>

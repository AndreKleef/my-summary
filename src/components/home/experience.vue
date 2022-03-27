<template>
  <div class="experiense">
    <h2 class="experiense__content-title subtitle">{{ msg }}</h2>
    <div class="experiense__block">
      <div class="experiense__container container">
        <div class="experiense__content">
          <div class="experiense__tabs">
            <span @click="selectTab(row.id)"
              v-for="row in content" :key="row"
              :class="{ 'active' : currentTab == row.id }"
              class="experiense__tabs-item">{{ row.title }}
            </span>
          </div>
          <div v-if="currentTab == 1" class="experiense__description">
            <p class="experiense__description-text text">Информационные технологии, системная интеграция, интернет</p>
            <p class="experiense__description-text text">Интернет-провайдер</p>
            <p class="experiense__description-text text">Разработка программного обеспечения</p>
            <p class="experiense__description-text text">Адаптивная верстка (html, css, jquery, js,)</p>
            <p class="experiense__description-text text">Верстка по макетам psd, макетам в figma и xd</p>
            <p class="experiense__description-text text">Полная посадка на Modx</p>
            <p class="experiense__description-text text">Редактирование в Wordpress</p>
          </div>
          <div v-if="currentTab == 2" class="experiense__description">
            <p class="experiense__description-text text">Информационные технологии, системная интеграция, интернет</p>
            <p class="experiense__description-text text">Интернет-компания (поисковики, платежные системы, соц.сети, информационно-познавательные и развлекательные ресурсы, продвижение сайтов и прочее)</p>
            <p class="experiense__description-text text">Разработка программного обеспечения</p>
            <p class="experiense__description-text text">Системная интеграция, автоматизации технологических и бизнес-процессов предприятия</p>
            <p class="experiense__description-text text">-Написание и редактирования функционала сайта на чистом javaScript</p>
            <p class="experiense__description-text text">-Адаптивная верстка для мобильных устройств.</p>
            <p class="experiense__description-text text">-Кросс-браузерная верстка</p>
            <p class="experiense__description-text text">-Валидная верстка сайта(соответствующая стандартам W3C)</p>
            <p class="experiense__description-text text">-Семантическая верстка</p>
            <p class="experiense__description-text text">-Оптимизация под поисковые системы</p>
            <p class="experiense__description-text text">-Оптимизация скорости загрузки сайта</p>
          </div>
          <div v-if="currentTab == 3" class="experiense__description">
            <p class="experiense__description-text text">Информационные технологии, системная интеграция, интернет</p>
            <p class="experiense__description-text text">Интернет-компания (поисковики, платежные системы, соц.сети, информационно-познавательные и развлекательные ресурсы, продвижение сайтов и прочее)</p>
            <p class="experiense__description-text text">Работа ограничена одним проектом</p>
            <p class="experiense__description-text text">Верстка новых страниц, блоков, элементов, писем по дизайну в figma</p>
            <p class="experiense__description-text text">Переписывание функционала с jquery на typescript</p>
            <p class="experiense__description-text text">Опыт работы с vue.js</p>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- <div v-for="row in content" :key="row"
        v-if="currentTab == row.id"
        class="content">
    <h2>{{ row.id }}</h2>
    <p>{{ row.content }}</p>
  </div> -->

</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    content: Array
  },
  data() {
    return {
      currentTab: 1
    }
  },
  methods:{
    selectTab(selectedTab) {
        this.currentTab = selectedTab
    }
  }
}
</script>

<style scoped lang="scss">

  .experiense {
    margin: 60px 0 0 0;

    &__block {
      background: url('../../assets/img/experiense.jpeg') no-repeat center/cover;
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
        right: 0;
        width: 50%;
        height: 100%;
        background: rgba(238, 238, 238, 0.65);
        z-index: 1;
      }
    }

    &__container {
      position: relative;
      height: 100%;
    }

    &__content {
      height: 100%;
      position: relative;
    }

    &__tabs {
      position: absolute;
      top: 0;
      right: 55%;
      width: 50%;
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      padding: 90px 0;
      z-index: 2;

      &-item {
        background: rgba(0, 0, 0, 0.8);
        color: #ffffff;
        text-transform: uppercase;
        font-size: 36px;
        font-weight: 900;
        padding: 8px 0 8px 16px;
        letter-spacing: 20px;
        margin: 20px 0;
        text-align: right;
        max-width: 360px;
        transition: 0.2s;
        cursor: pointer;

        &.active {
          background: rgba(196, 196, 196, 0.2);
        }
      }
    }

    &__description {
      position: absolute;
      top: 0;
      left: 55%;
      width: 50%;
      z-index: 2;
      padding: 90px 15px 90px 0;
      max-height: 420px;
      overflow-y: auto;

      &::-webkit-scrollbar {
        width: 5px;
        background-color: rgba(26, 24, 47, 0.15);
        border-radius: 5px;
      }

      &::-webkit-scrollbar-thumb {
          background: #cccccc;
          border-radius: 5px;
      }

      &-text {
        padding: 8px 0;
        letter-spacing: 1px;
      }
    }
  }

</style>

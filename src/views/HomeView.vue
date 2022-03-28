<template>
  <div class="home">
    <promo msg="Добро пожаловать на мою страницу"/>
    <skills msg="Мои ключевые навыки"/>
    <experience msg="Мой личный опыт" :content="tabData"></experience>
  </div>
</template>

<script>
  import promo from '@/components/home/promo.vue'
  import skills from '@/components/home/skills.vue'
  import experience from '@/components/home/experience.vue'

  export default {
    name: 'HomeView',
    components: {
      promo,
      skills,
      experience
    },
    data() {
      return {
        tabData: [
          {
            title: 'ASAP',
            id: 1,
            content:
            '- Адаптивная верстка (html, css, jquery, js,)' + '<br>' +
            '- Верстка по макетам psd, макетам в figma и xd' + '<br>' +
            '- Полная посадка на Modx' + '<br>' +
            '- Редактирование в Wordpress'
          },
          {
            title: 'SPACEAPP',
            id: 2,
            content:
            '- Написание и редактирования функционала сайта на чистом javaScript' + '<br>' +
            '- Адаптивная верстка для мобильных устройств' + '<br>' +
            '- Кросс-браузерная верстка' + '<br>' +
            '- Валидная верстка сайта(соответствующая стандартам W3C' + '<br>' +
            '- Семантическая верстка' + '<br>' +
            '- Оптимизация под поисковые системы' + '<br>' +
            '- Оптимизация скорости загрузки сайта'
          },
          {
            title: 'LEGALBET',
            id: 3,
            content:
            '- Работа ограничена одним проектом (WebPack)' + '<br>' +
            '- Верстка новых страниц, блоков, элементов, писем по дизайну в figma' + '<br>' +
            '- Переписывание функционала с jquery и js на typescript' + '<br>' +
            '- Опыт работы с vue.js'
          }
        ]
      }
    }
  }
</script>

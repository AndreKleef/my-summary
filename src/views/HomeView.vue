<template>
  <div class="home">
    <mainPromo title="Добро пожаловать на мою страницу"/>
    <mySkills title="Мои ключевые навыки"/>
    <myExperience title="Мой личный опыт" :content="tabData"></myExperience>
  </div>
</template>

<script>
  import mainPromo from '@/components/home/mainPromo.vue'
  import mySkills from '@/components/home/mySkills.vue'
  import myExperience from '@/components/home/myExperience.vue'

  export default {
    name: 'HomeView',
    components: {
      mainPromo,
      mySkills,
      myExperience
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

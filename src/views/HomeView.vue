<template>
  <div class="home">
    <promo msg="Добро пожаловать на мою страницу"/>
    <skills msg="Мои ключевые навыки"/>
    <experience msg="Мой личный опыт" :content="tabData"></experience>
  </div>
</template>

<script>
// @ is an alias to /src
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
          content: 'Описание №1'
        },
        {
          title: 'SPACEAPP',
          id: 2,
          content: 'Описание №2'
        },
        {
          title: 'LEGALBET',
          id: 3,
          content: 'Описание №3'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="home">
    <promo msg="Добро пожаловать на мою страницу"/>
    <skills msg="Мои ключевые навыки"/>
  </div>
</template>

<script>
// @ is an alias to /src
import promo from '@/components/home/promo.vue'
import skills from '@/components/home/skills.vue'

export default {
  name: 'HomeView',
  components: {
    promo,
    skills,
  }
}
</script>

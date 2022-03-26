<template>
  <div class="home">

    <testChallenge msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import testChallenge from '@/components/testChallenge.vue'

export default {
  name: 'HomeView',
  components: {
    testChallenge
  }
}
</script>

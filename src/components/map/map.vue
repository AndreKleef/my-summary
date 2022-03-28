<template>
  <div class="hello">
    <h1 class="subtitle">{{ msg }}</h1>

    <yandex-map :settings="settings">
        <!--Markers-->
    </yandex-map>
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

</style>

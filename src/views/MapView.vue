<template>
  <div class="map">
    <mapTemplate title="Мое местоположение"/>
  </div>
</template>

<script>
  import mapTemplate from '@/components/map/mapTemplate.vue'

  export default {
    name: 'MapView',
    components: {
      mapTemplate
    }
  }
</script>

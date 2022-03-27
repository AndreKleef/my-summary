<template>
  <div class="map">
    <mapTemplate msg="Мое местоположение"/>
  </div>
</template>

<script>

import mapTemplate from '@/components/map/map.vue'

export default {
  name: 'MapView',
  components: {
    mapTemplate,
  }
}
</script>

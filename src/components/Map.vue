<template>
  <div id="map"></div>
</template>

<script setup>
import { onMounted } from 'vue'
import { Map, View } from 'ol'
import { OSM } from 'ol/source'
import { Tile } from 'ol/layer'
import 'ol/ol.css'

onMounted(() => {
  const map = new Map({
    target: 'map',
    view: new View({
      center: [0, 0],
      zoom: 0
    }),
    layers: [
      new Tile({
        source: new OSM()
      })
    ]
  })
})
</script>

<style scoped>
#map {
  position: absolute;
  top: 0;
  bottom: 0;
  width: 100%;
}
</style>

<style>
.ol-attribution {
  font-size: 8px;
}
</style>
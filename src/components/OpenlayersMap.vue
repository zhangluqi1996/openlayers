<template>
  <div id="map" style="width:1200px;height:600px;"></div>
</template>

<script>
  import 'ol/ol.css'
  import {Map,View} from 'ol'
  import TileLayer from 'ol/layer/Tile'
  import OSM from 'ol/source/OSM'

  export default {
  mounted() {
    this.initMap();
  },
  methods: {
    //---地图初始化---
    initMap() {
      new Map({
        target: "map",
        layers: [
          new TileLayer({
            source: new OSM()
          })
        ],
        view: new View({
          projection: "EPSG:4326",
          center: [118.51064429904429, 37.42444378968362],
          zoom: 5
        })
      })
    }
  }
}
</script>

<style scoped>
  #map {
    height: 100%;
  }
</style>

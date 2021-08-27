<template>
  <div v-if="currentPage==='home'">
    <button @click="currentPage='counter'">Counter</button>
    <button @click="currentPage='map'">Map</button>
  </div>
  <div v-else>
    <button @click="currentPage='home'" id="home">Home</button>
    <Counter v-if="currentPage==='counter'" />
    <Map v-if="currentPage==='map'" />
  </div>
</template>

<script setup>
import Counter from './Counter.vue'
import Map from './Map.vue'
import { ref } from 'vue'

const currentPage = ref('home')
</script>

<style scoped>
button {
  font-size: 1.5em;
  font-family: 'Courier New', Courier, monospace;
  padding: 12px 20px;
  margin: 5px;
}
</style>
<template>
  <div class='count'>{{ count }}</div>
  <button @click='count--'>-</button>
  <button @click='count++'>+</button>
</template>

<script setup>
import { ref } from 'vue';

const count = ref(0);
</script>

<style scoped>
.count {
  font-size: 5em;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif
}

button {
  font-size: 2em;
  font-family: 'Courier New', Courier, monospace;
  padding: 12px 20px;
  margin: 5px;
}
</style>

<template>
  <div id="app">
    <WorldWeather/>
  </div>
</template>

<script>
import WorldWeather from './components/WorldWeather.vue'

export default {
  name: 'App',
  components: {
    WorldWeather
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

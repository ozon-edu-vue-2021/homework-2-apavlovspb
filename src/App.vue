<template>
  <div id="app">
    <Map/>
    <Printer/>
  </div>
</template>

<script>
import Printer from './components/Printer.vue'
import Map from './components/Map.vue'
 

export default {
  name: 'App',
  components: {
    Printer,Map
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
  margin-top: 30px;
}
</style>

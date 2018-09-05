<template>
  <div id="app">

    <Equipo />

  </div>
</template>

<script>

import Equipo from "./components/Equipo.vue";


export default {
  name: 'app',
  components: {
    Equipo
  }
}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<template>
  <div id="app">

    <b-container>
      <b-row>
        <b-col v-for="(equipo, index) in equipos" :key='index'>
           <Equipo :info="equipo" />
        </b-col>
      </b-row>
    </b-container>



  </div>
</template>

<script>

import Equipo from "./components/Equipo.vue";


export default {
  name: 'app',
  components: {
    Equipo
  },
  data() {
    return {
      equipos: [
        {
          nombre: "Equipo 1",
          logo:
            "https://via.placeholder.com/600x300/D2B48C/ffffff?text=Logo+equipo",
          estado: true,
          jugadores: [{ jugador: "1" }]
        },
        {
          nombre: "Equipo 2",
          logo:
            "https://via.placeholder.com/600x300/D2B48C/ffffff?text=Logo+equipo",
          estado: false,
          jugadores: [{ jugador: "1" }, { jugador: "1" }]
        },
        {
          nombre: "Equipo 3",
          logo:
            "https://via.placeholder.com/600x300/D2B48C/ffffff?text=Logo+equipo",
          estado: true,
          jugadores: [{ jugador: "1" }, { jugador: "1" }, { jugador: "1" }]
        },
        {
          nombre: "Equipo 4",
          logo:
            "https://via.placeholder.com/600x300/D2B48C/ffffff?text=Logo+equipo",
          estado: false,
          jugadores: []
        },
        {
          nombre: "Equipo 5",
          logo:
            "https://via.placeholder.com/600x300/D2B48C/ffffff?text=Logo+equipo",
          estado: true,
          jugadores: [{ jugador: "1" }, { jugador: "1" }]
        }
      ]
   }
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

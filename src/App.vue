<template>
  <div id="app">

    <b-container>
      <b-row>
        <b-col>
          <b-button v-b-modal="'myModal'" variant="success" class="float-right new-btn">
            <v-icon class="icon" name="plus" />
            Agregar Equipo
          </b-button>
        </b-col>
      </b-row>
      <b-row>
        <b-col v-for="(equipo, index) in equipos" :key='index'>
          <Equipo :info="equipo" />
        </b-col>
      </b-row>
    </b-container>



  <equipo-frm @new_team="onNewteam"></equipo-frm>

  </div>
</template>

<script>

import Equipo from "./components/Equipo.vue";
import FormEquipo from "./components/forms/Equipo.vue";


export default {
  name: 'app',
  components: {
    Equipo,
    "equipo-frm": FormEquipo
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
  },
  methods:{
    onNewteam(equipo) {
      this.equipos.push(Object.assign({}, equipo));
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

.new-btn {
  margin-bottom: 10px;
}

.icon {
  margin-right: 5px;
}

.mymodal-footer {
  display: none !important;
}
</style>

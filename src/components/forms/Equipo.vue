<template>
  <b-modal id="myModal" title="Nuevo Equipo" body-class="mymodal-body" footer-class="mymodal-footer">

    <b-form v-if="show">
      <b-form-group label="Nombre:" description="Escribe el nombre del equipo">
        <b-form-input v-model="form.nombre"
                        required
                        placeholder="Nombre de equipo">
        </b-form-input>
      </b-form-group>
      <b-form-group label="Logo:" description="Escribe la url del logo">
        <b-form-input v-model="form.logo"
                        required
                        placeholder="Escribe la url">
        </b-form-input>
      </b-form-group>
      <b-form-group label="Jugadores:" description="Selecciona un jugador">
        <b-form-select :options="jugadores"
                        required multiple
                        v-model="form.jugadores">
          </b-form-select>
      </b-form-group>
      <b-form-group >
          <b-form-radio-group v-model="form.estado">
            <b-form-radio value="false">Inactivo</b-form-radio>
            <b-form-radio value="true">Activo</b-form-radio>
          </b-form-radio-group>
        </b-form-group>
    </b-form>

    <div slot="modal-footer">
      </div>
  </b-modal>
</template>

<script>
export default {
  data() {
    return {
      form: {
        nombre: "",
        logo: "",
        jugadores: [],
        estado: false
      },
      jugadores: [
        "Jugador 1",
        "Jugador 2",
        "Jugador 3",
        "Jugador 4",
        "Jugador 5"
      ],
      show: true
    }
  }
}
</script>

<style>
.mymodal-body .col-form-label {
  text-align: left;
}

.mymodal-body .text-muted {
  text-align: right;
}
</style>
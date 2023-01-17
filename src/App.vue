<template>
  <div id="app" class="container">
    <div class="row">
      <div class="col-md-12 mt-2">
        <h1>Usuarios</h1>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      usuarios: [],
    }
  },
    methods: {
      getUsuarios() {
        // Método para obtener la lista de usuarios
      },
      postUsuario() {
        // Método para crear un usuario
      },
      putUsuario() {
        // Método para actualizar un usuario
      },
      deleteUsuario() {
        // Método para borrar un usuario
      },
    },
    mounted() {
      this.getUsuarios();
    }
  }
</script>
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
        try {
          const response = await fetch('https://jsonplaceholder.typicode.com/users');
          this.usuarios = await response.json();
        } catch (error) {
          console.error(error);
        }
      },
      postUsuario() {
          try {
            const response = await fetch('https://jsonplaceholder.typicode.com/users', {
            method: 'POST',
            body: JSON.stringify(usuarios),
            headers: { 'Content-type': 'application/json; charset=UTF-8' },
            });
            const usuarioCreado = await response.json();
            this.usuarios = [...this.usuarios, usuarioCreado];
          } catch (error) {
          console.error(error);
          }
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
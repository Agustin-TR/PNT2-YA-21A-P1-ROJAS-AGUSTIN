<template>
  <div class="container-fluid mt-3">
    <div class="card">
      <div class="card-header">
        <header>
          <h2>Parcial de Agustín Rojas</h2>
        </header>
      </div>

      <div class="card-body">
        <main>
          <Conversor />
          <Respuestas />

        </main>
      </div>
    </div>
  </div>
</template>

<script>
  import Conversor from './components/Conversor.vue'
  import Respuestas from './components/Respuestas.vue'


  export default {
    name: 'App',
    components: {
      Conversor,
      Respuestas,
    }
  }

</script>

<style scoped>
.card-header {
  background-color: rgb(23, 62, 113);
  color: white;
}
</style>

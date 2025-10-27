<template>
  <section class="card-r">
    <div class="card-header-r">
      <h2>Respuestas</h2>
    </div>

    <div class="card-body-r">
      <div class="table-responsive">
        <table class="table table-dark">
          <thead>
            <tr>
              <th>Pregunta</th>
              <th>Respuesta</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>1</td>
              <td>c</td>
            </tr>
            <tr>
              <td>2</td>
              <td>c</td>
            </tr>
            <tr>
              <td>3</td>
              <td>a</td>
            </tr>
          </tbody>
        </table>
      </div>

    </div>
    </section>

</template>

<script>

export default {
  name: 'respuestas',
  props: [],
  mounted() {

  },
  data() {
    return {

    }
  },
  methods: {

  },
  computed: {

  }
}
</script>

<style scoped>
/*<!-- Respuestas -->*/

.card-r {
  padding: 1rem;
  margin: 2rem auto;
  max-width: 700px;
  font-family: 'Segoe UI', sans-serif;
}

.card-header-r {
  background-color: #60152a;
  color: #fff;
  padding: 0.75rem 1rem;
  text-align: center;
  font-size: 1.5rem;
  font-weight: bold;
}

.card-body-r {
  padding: 1rem;
}

.table {
  width: 100%;
  border-collapse: collapse;
  border-radius: 8px;
  overflow: hidden;
}

.table th,
.table td {
  padding: 0.75rem;
  text-align: left;
}

.table th {
  background-color: #9e9ea6;
  color: #333;
}
</style>

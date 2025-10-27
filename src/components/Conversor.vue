<template>
  <section class="card">
    <div class="card-header">
      <h2>Conversor de temperatura</h2>
    </div>

    <div class="card-body">
      <form>
        <!-- campo celsius-->
        <div class="form-group">
          <label for="temp">Temperatura en °C</label>
          <input id="temp-c" type="number" class="form-control" placeholder="Ingrese la temperatura"
            v-model.number="formData.temp">
        </div>

        <div class="form-group">
          <label for="temp-f">Conversión en °F</label>
          <p v-show="true" :style="{ color: colorTemp }">{{ conversionFahrenheit }}</p>
        </div>

        <div class="form-group">
          <label for="temp-k">Conversión en °K</label>
          <p v-show="true" :style="{ color: colorTemp }">{{ conversionKelvin }}</p>
        </div>

      </form>



    </div>

  </section>


</template>

<script>
export default {
  name: 'Conversor',

  data() {
    return {
      // estado local
      formData: this.getInicialData(),
      formDirty: this.getInicialData(),
    };
  },
  computed: {
    // propiedades derivadas
    colorTemp() {
      const t = this.formData.temp
      if (t <= 0) return 'blue'
      if (t > 0 && t < 15) return 'magenta'
      return 'red'
    },
    conversionFahrenheit() {
      const temp = this.formData.temp
      if (temp === null || temp === '') {
        return ''
      }

      const fahrenheit = (temp * 9) / 5 + 32
      return `${fahrenheit.toFixed(2)} °F`
    },
    conversionKelvin() {
      const temp = this.formData.temp
      if (temp === null || temp === '') {
        return ''
      }
      const kelvin = temp + 273.15
      return `${kelvin.toFixed(2)} °K`
    },
  },

  watch: {

  },
  methods: {
    getInicialData() {
      return {
        temp: null,
      }
    },
  },
};

</script>

<style scoped>
.card {
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  background-color: #f8f9fa;
}

.card-header {
  background: #066782;
  color: white;
  padding: 1rem 1.5rem;
  border-bottom: none;
}

.card-header h2 {
  margin: 0;
  font-weight: 600;
  letter-spacing: 0.5px;
}

.card-body {
  padding: 2rem;
}

/* ------------------------------------------------------------------ */
/* CLASES DEL FORMULARIO */

.form-group {
  margin-bottom: 1.5rem;
}

.form-control {
  border-radius: 8px;
  transition: border-color 0.3s ease, box-shadow 0.3s ease;
  width: 100%; 
  padding: 0.375rem 0.75rem; 
  border: 1px solid #ced4da; 
}

.form-control:focus {
  border-color: #00c6ff;
  box-shadow: 0 0 0 0.2rem rgba(0, 198, 255, 0.25);
  outline: none; 
}


.form-group p {
  min-height: 1.2em; 
  margin-top: 0.5rem; 
  margin-bottom: 0;
  font-size: 1.1rem;
}


</style>
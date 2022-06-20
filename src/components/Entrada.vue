<template>
  <div v-bind:class="{'card border-warning mb-3': isActive, 'card border-danger mb-3': isActiveDanger}"
    class="card text-bg-dark bg-dark mb-3 text-white"
    style="max-width: 18rem"
  >
    <h5 class="card-header">{{ title }}</h5>
    <div class="card-body p-3">
      <h5 class="card-title">Fecha: {{ fecha }}</h5>
      <p class="card-text">${{ precio }}</p>
      <p>Cantidad comprada: {{ cantidadComprada }}/{{ cantidadDisponible }}</p>
      <p>Recaudacion: {{recaudacion}}</p>
      <button @Click="comprarEntrada()" class="btn btn-success">Comprar</button>
      <div v-if="(this.cantidadDisponible - this.cantidadComprada <= 5 && this.cantidadDisponible - this.cantidadComprada != 0)" class="alert alert-warning mt-3" role="alert">
      Ultimas {{ this.cantidadDisponible - this.cantidadComprada }} entradas disponibles!
      </div>
      <div v-if="(this.cantidadDisponible - this.cantidadComprada == 0)" class="alert alert-danger mt-3" role="alert">
      No quedan mas entradas!
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    fecha: String,
    precio: Number,
    cantidadDisponible : Number
  },
  data() {
    return {
      cantidadComprada: 0,
    };
  },
  computed: {
    recaudacion() {
      return this.cantidadComprada * this.precio;
    },
  },
  methods: {
    comprarEntrada() {
      if (this.cantidadComprada < this.cantidadDisponible) {
        this.cantidadComprada = this.cantidadComprada + 1;
      } 
      if(this.cantidadComprada == (this.cantidadDisponible - 5)) {
        this.isActive = true;
      }
      else if (this.cantidadComprada == this.cantidadDisponible){
        this.isActiveDanger = true;
      }
    },
  },
};
</script>

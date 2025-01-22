<template>
    <main>
      <h1>Lista de Frutas</h1>
      <!-- Enviar la lista al hijo y escuchar la selección -->
      <ComponenteHijo :listaPro="frutas" @seleccionar="manejarSeleccion" />
  
      <!-- Mostrar la fruta seleccionada -->
      <p v-if="frutaSeleccionada">
        Fruta seleccionada: <p>{{ frutaSeleccionada }}</p>
      </p>
    </main>
  </template>
  
  <script>
  import ComponenteHijo from '@/components/ComponenteHijo.vue';
  
  export default {
    components: {
      ComponenteHijo,
    },
    data() {
      return {
        frutas: ['Pera', 'Manzana', 'Plátano', 'Uva','fresa','kiwi','mandarina'], // Lista enviada al hijo
        frutaSeleccionada: null, // Fruta seleccionada por el hijo
      };
    },
    methods: {
      manejarSeleccion(fruta) {
        this.frutaSeleccionada = fruta; // Actualizar la fruta seleccionada
      },
    },
  };
  </script>
  
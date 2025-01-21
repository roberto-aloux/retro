<template>
    <div>
      <v-select
        :items="listaPro"
        label="Selecciona una fruta"
        @change="seleccionar"
      ></v-select>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      listaPro: {
        type: Array,
        required: true, 
      },
    },
    methods: {
      seleccionar(fruta) {
        // Emitir la fruta que se selecciono al padre 
        this.$emit('seleccionar', fruta);
      },
    },
  };
  </script>
  
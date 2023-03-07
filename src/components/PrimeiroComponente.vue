<template>
  <div>
    <h1>Ola Vue</h1>
    <h2>Meu nome é: {{ nome }}</h2>
    <h2>Profissao: {{ nome }}</h2>
    <MultiplosEventos/>
    <p>-----------------------------------</p>
  </div>
</template>


<script>

import MultiplosEventos from './MultiplosEventos.vue'

export default {
  name: "Primeiro Componente",
  components:{
    MultiplosEventos
  },
  data() {
    return {
      nome: "Erik",
      profissao: "Programador",
    };
  },
};
</script>

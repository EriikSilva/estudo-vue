<template>
  <h2>Descrição da pessoa: {{ nome }}</h2>
  <Info :email="email" />
</template>

<script>
import Info from "../components/Info.vue";

export default {
  name: "Pessoa",
  components: {
    Info,
  },
  props:{
    email:String
  },
  data() {
    return {
      nome: "erik",
      email:"teste@teste.com"
    };
  },
};
</script>

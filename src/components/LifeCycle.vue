<template>
  <h1>Meu Nome é:{{ nome }}</h1>
</template>


<script>
export default {
  name: "LifeCycle",
  data() {
    return {
      nome: "Ainda n sei",
    };
  },
  created() {
    setTimeout(() => {
      this.nome = "matheus";
    }, 3000);
  },
  mounted() {
    setTimeout(() => {
      this.nome = "pedro";
    }, 2000);
  },
};
</script>

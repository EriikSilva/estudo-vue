<template>
  <div>
    <p>{{ email }}</p>
    <PrimeiroComponente />
    <p v-if="trabalhando">Trabalho:</p>
    <p v-else>em busca de Trabalho</p>
    <p>Tecnologia backend:</p>
    <ul>
      <li v-for="(tecnology, index) in backendTecnologies" v-bind:key="index">
        {{ tecnology }}
      </li>
    </ul>
    <p>Utilizo as seguintes tecnologias para frontend</p>
    <ul>
      <li v-for="tecnology in frontendTecnologies" :key="tecnology.id">
        {{ tecnology.language }}
      </li>
    </ul>
    <p v-show="mostrar_email">Mostrar email: {{ email }}</p>
    <p>Acessar portifolio <a v-bind:href="link" target="blank">AQUI</a></p>
    <Picture />
    <div>
      <button @click="mostrarEmail">
        {{ textoBotao }}
      </button>
      <Form />
    </div>
  </div>
</template>

<script>
import Picture from "./Picture.vue";
import Form from "./Form.vue";
import PrimeiroComponente from "./PrimeiroComponente.vue";

export default {
  name: "Info",
  components: {
    Picture,
    Form,
    PrimeiroComponente,
  },
  props: {
    email:String
  },
  data() {
    return {
      trabalhando: true,
      mostrar_email: false,
      // email: "erik@teste.com",
      link: "https://google.com",
      textoBotao: "Mostrar Email",
      backendTecnologies: ["Javascript", "PHP", "Python"],
      frontendTecnologies: [
        { id: 1, language: "HTML" },
        { id: 2, language: "CSS" },
        { id: 3, language: "VUE" },
      ],
    };
  },
  methods: {
    mostrarEmail() {
      this.mostrar_email = !this.mostrar_email;

      if (!this.mostrar_email) {
        this.textoBotao = "Mostar Email";
      } else {
        this.textoBotao = "Esconder Email";
      }
    },
  },
};
</script>
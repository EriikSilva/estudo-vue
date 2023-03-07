<template>
  <div>
    <button
      @click="primeiro(txt1, $event), segundo(txt2, $event), terceiro(txt3)"
    >
      Ativar Multiplos Eventos
    </button>
    <p>{{ multiplos_eventos }}</p>
  </div>
</template>

<script>
export default {
  name: "MultiplosEventos",
  data() {
    return {
      multiplos_eventos: "",
      txt1: "Primeiro Evento",
      txt2: "Segundo Evento",
      txt3: "",
    };
  },
  methods: {
    primeiro(txt1, e) {
      this.multiplos_eventos = txt1;
    },

    segundo(txt2, e) {
      setTimeout(() => (this.multiplos_eventos = txt2), 1000);
    },
    terceiro() {
      setTimeout(() => (this.multiplos_eventos = ""), 3000);
    },
  },
};
</script>
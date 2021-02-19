<template>
  <nav class="navbar navbar-expand-lg navbar-bytebank">
    <a class="navbar-brand" href="#">ByteBank</a>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <barra-navegacao-logado v-if="usuarioestaLogado"></barra-navegacao-logado>
      <barra-navegacao-deslogado v-else></barra-navegacao-deslogado>
    </div>
  </nav>
</template>

<script>
import BarraNavegacaoDeslogado from "./BarraNavegacaoDeslogado.vue";
import BarraNavegacaoLogado from "./BarraNavegacaoLogado.vue";

export default {
  components: { BarraNavegacaoLogado, BarraNavegacaoDeslogado },
  computed: {
    usuarioestaLogado() {
      return Boolean(this.$store.state.token);
    }
  }
};
</script>

<style>
.navbar {
  background: #27ae60;
}
.navbar-bytebank a {
  color: #fff;
}
.navbar-bytebank a:hover {
  color: #000;
}
</style>

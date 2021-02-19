<template>
  <div id="app">
    <barra-navegacao></barra-navegacao>
    <router-view />
  </div>
</template>

<script>
import BarraNavegacao from "@/components/BarraNavegacao";
export default {
  components: {
    BarraNavegacao
  }
};
</script>

<style></style>

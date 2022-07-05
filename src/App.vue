<template>
  <h1>COMPONENTE RAÍZ</h1>
  <Persona />
  <!-- <Opciones />
  <Composition /> -->
</template>

<script>
import Persona from "./components/Persona.vue";
/* import Opciones from "./components/Opciones.vue";
import Composition from "./components/Composition.vue"; */
export default {
  name:"App",
  components:{
    /* Opciones,
    Composition */
    Persona
  }
}
</script>

<style>
</style>

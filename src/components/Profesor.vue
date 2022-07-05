<template>
  <h1>Componente Profesor</h1>
  <h3>Valor de la variable nombre: {{nombre}}</h3>

  <button type="button" class="btn btn-secondary" @click="aumentar">Aumentar</button>
</template>

<script>
export default {
    name:"Profesor",

    props:{
        nombre:{
            type:String,
            default:"No se envío nada",
        },
        aumentar:Function,
    }

}
</script>

<style>

</style>
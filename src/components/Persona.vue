<template>
  <h1>Componente Persona</h1>
  <Profesor :nombre="nombre" :aumentar="aumentar"/>
</template>

<script>
import Profesor from "./Profesor.vue";
export default {
    name:"Persona",

    components:{
        Profesor,
    },

    setup(){
        let nombre="Vitervo";
        const paterno="Lopez";
        const materias=["LENP","ADDA"];
        const peliculas={
            titulo:"FOREST",
            genero:"MOTIVACIÓN"
        };

        const aumentar=()=>{
            console.log("aumentando...");
        }

        return{
            nombre,
            paterno,
            materias,
            peliculas,
            aumentar
        }
    }

}
</script>

<style>

</style>
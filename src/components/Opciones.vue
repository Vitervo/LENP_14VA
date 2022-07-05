<template>
  <h1>Bienvenidos a mi API de opciones</h1>

  <p>Nombre: {{nombre}}</p>
  <p>Apelido paterno:{{paterno}}</p>
  <p>Apellido materno:{{materno}}</p>
  <p>Materias:{{materias[2]}}</p>
  <p>Edad:{{edad}}</p>
  <p>Potencia:{{potencia}}</p>
  <p>Peliculas:{{peliculas.titulo}}</p>

  <button type="button" @click="aumentar(10)" class="btn btn-primary">Aumentar</button>
  <button type="button" @click="disminuir(5)" class="btn btn-secondary">Disminuir</button>
</template>

<script>
export default {
    name:"Opciones",

    data(){
      return{
        nombre:"Vitervo",
        paterno:"López",
        materno:"Caballero",
        materias:["ADDA","LENP","ESTADÍA"],
        edad:36,
        potencia:98.50,
        peliculas:{
          genero:"Comedia",
          titulo:"El señor de los niños"
        }
      }
    },

    methods:{
      aumentar(newVal){
        this.edad=this.edad+newVal;
      },
      disminuir(newVal){
        this.edad=this.edad-newVal;
      }
    }

}
</script>
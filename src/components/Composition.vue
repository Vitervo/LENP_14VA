<template>
  <h1>Bienvenido a mi API de composicion</h1>
  <p>Nombre: {{ nombre }}</p>
  <p>Apelido paterno:{{ paterno }}</p>
  <p>Apellido materno:{{ materno }}</p>
  <p>Materias:{{ materias[2] }}</p>
  <p>Edad:{{ edad }}</p>
  <p>Potencia:{{ potencia }}</p>
  <p>Peliculas:{{ peliculas.titulo }}</p>

  <p>Materias</p>
  <span v-for="(mat, index) in materias" :key="index">
    {{ mat }}--{{ index }}--
  </span>

  <p>MATERIAS EN LISTA</p>
  <u>
    <template v-for="(temp, index) in datos" :key="index">
      <!-- <li v-if="temp<=10">
                {{index}}--{{temp}}
            </li>
            <li v-else-if="temp===100">
                {{index}}--{{temp}}
            </li> -->
    </template>
  </u>
  <button type="button" class="btn btn-primary" @click="aumentar(10)">Aumentar</button>
  <button type="button" class="btn btn-secondary" @click="disminuir(5)">Disminuir</button>

</template>
<script>
import {ref} from "vue";
export default {
  name: "Composition",
  setup() {
    const datos = [12, 15, 6, 8, 9, 50, 100, 200, 300];
    const nombre = "Vitervo";
    const paterno = "López";
    const materno = "Caballero";
    const materias = ["ADDA", "LENP", "ESTADÍA"];
    let edad = ref(36);
    const potencia = 98.5;
    const peliculas = {
      genero: "Comedia",
      titulo: "El señor de los niños",
    };

    const aumentar=(newVal)=>{
      edad.value=edad.value+newVal;
    };

    const disminuir=(newVal)=>{
      edad.value=edad.value-newVal;
    };


    return {
      nombre,
      paterno,
      materno,
      materias,
      edad,
      potencia,
      peliculas,
      datos,
      aumentar,
      disminuir
    };
  },
};
</script>

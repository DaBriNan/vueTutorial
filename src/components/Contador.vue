
<template>
  <h1> hola mundo</h1>
 <p> {{ contador }}</p>
  <button @click="incrementar">Incrementar</button> 
  <button @click="decrementar">Decrementar</button> 
</template>

<script setup>

import {ref} from 'vue'; //mandamos llamara ref, funcion para crear una referencia reactiva a un valor
const contador=ref(0); //creamos la variable reactiva

const incrementar= () =>{ //funcion de incrementar el contador
  contador.value++;
}

const decrementar= () =>{ //funcion de decrementar el contador
  contador.value--;
}
</script>


<style scoped>

p{
  color:rgb(0, 162, 255)
}
 button{
  color: rgb(91, 126, 160);
 }

</style>

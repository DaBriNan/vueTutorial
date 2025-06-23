<template>
    <div>
        <h2> Lista de tareas</h2>
        <input type="text" v-model="nuevaTarea" @keyup.enter="addTarea">
        <ul>
            <li v-for="(tarea,index) in tarea" :key="index">
                {{ tarea }}
            </li>
        </ul>
    </div>
</template>

<script setup> 

import {ref} from 'vue';
const tarea=ref([]);
const nuevaTarea=ref('');
const addTarea= () =>{
    tarea.value.push(nuevaTarea.value); //v-model manda llamar la variable reactiva
    nuevaTarea.value='';//cuando lo escribimos se resetea
}

</script>

<style>
</style>
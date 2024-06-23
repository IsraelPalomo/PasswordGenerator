<template>
  <div class="card">
    <p>{{ password }}</p>
    <Button @btnAction="generate"/>
  </div>
</template>

<script setup>
import Button from './Button.vue'
import {ref} from 'vue'

const password = ref('');

function generate(){
    console.log('...')
    // Definir el conjunto de caracteres: letras (mayúsculas y minúsculas), números y símbolos
    const caracteres = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*()_+-=[]{}|;:,.<>?';

    // Inicializar la contraseña como una cadena vacía
    let contraseña = '';

    // Seleccionar 5 caracteres aleatorios del conjunto de caracteres
    for (let i = 0; i < 5; i++) {
        const indiceAleatorio = Math.floor(Math.random() * caracteres.length);
        contraseña += caracteres[indiceAleatorio];
    }

    console.log(contraseña)

    password.value =  contraseña;
}

</script>

<style lang="css" scoped>
.card{
    padding: 1.5rem;
    background-color: #323232;
}
</style>
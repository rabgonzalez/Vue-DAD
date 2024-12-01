<template>
    <div class="container border border-0 rounded-5 bg-light p-5 info">
        <div class="row">
            <h1 v-if="palabra == 'hola'">Hola :)</h1>
            <h1 v-if="palabra == 'adios'">Adios :(</h1>
        </div>
        <button @click="cambiar" class="btn btn-primary mt-2">{{ (palabra == 'hola') ? 'Salir' : 'Entrar' }}</button>
        <div class="row mt-3">
            <p>Palabra actual: {{ palabra }}</p>
            <p v-pre class="text-danger">Palabra actual: {{ palabra }}</p>
        </div>
    </div>
</template>

<script setup>
    import { ref } from 'vue';

    const palabra = ref('hola');

    const cambiar = () => {
        palabra.value = (palabra.value == 'hola') ? 'adios' : 'hola';
    }
</script>

<style lang="css">
    .info {
        width: 300px;
        text-align: center;
        box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.2);
    }
</style>
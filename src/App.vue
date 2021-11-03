<template>
    <div id="app">
        <Titulo msg="Crear una nueva tarea"></Titulo>
        <Rellenar></Rellenar>
    </div>
</template>

<script>
import Titulo from './components/Titulo.vue';
import Rellenar from './components/Rellenar.vue';

export default {
    name: 'App',
    components: {
        Titulo,
        Rellenar
    }
}
</script>

<style scoped>
#app {
    text-align: center;
    color: #722da0;
    margin-top: 70px;
}
</style>
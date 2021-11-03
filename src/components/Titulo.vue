<template>
    <div class="titulo">
        <h1>{{ msg }}</h1>
    </div>
</template>

<script>
export default {
    name: 'Titulo',
    props: {
        msg: String
    }
}
</script>

<style scoped>
    .titulo h1 {
        font-size: 2.3em;
        margin-bottom: 1em;
    }
</style>
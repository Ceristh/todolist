<template>
    <div class="rellenar">
        <label for="input">Tarea: </label>
        <input id="input" type="text" placeholder="Ingrese nueva tarea" v-model="nuevaLista">
        <button v-on:click="AgregarTarea">Crear</button>
        <h3 class="my-5">Lista de tareas - Cristopher</h3>
        <ul>
            <li v-for="(lista, index) in agregar" :key="index">
                <div class="row">
                    <div class="col-md-10">
                        {{ index + 1 }}: {{lista}}
                    </div>
                    <div class="col-md-2 my-1">
                        <button v-on:click="remove(index)" class="remove">Remove</button>
                    </div>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'Rellenar',
        data: () => ({
            nuevaLista: "",
            agregar: []
        }),
        methods: {
            AgregarTarea() {
                this.agregar.push(this.nuevaLista);
                this.nuevaLista = ""; 
            },
            remove(id){
                this.agregar.splice(id,1);
            }   
        }
    };
</script>

<style scoped>
.rellenar input, button {
    padding: 6px;
}
.rellenar input {
    border: 1.5px solid #8b2d2d;
}
.rellenar button {
    background-color: #76a1e6;
    border: 1.5px solid #3d1a8d;
    margin-left: 1px;
    cursor: pointer;
    text-align: right;
}
.rellenar ul {
    width: 20%;
    margin: 0 auto;
    text-align: center;
    padding: 0;
}
</style>
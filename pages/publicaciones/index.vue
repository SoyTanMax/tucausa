<template>
    <div class="publicaciones">
        <div class="section">
            <div class="container">
                <p class="title">Mis proyectos</p>
                <nuxt-link :to="'/create'" class="button">Crear una publicación</nuxt-link>
            </div>
            <table class="table is-fullwidth">
                <tr>
                    <th>Nombre del proyecto</th>
                    <th>Fecha de creación</th>
                    <th>Fecha de publicación</th>
                    <th>Estatus</th>
                    <th></th>
                    <th></th>
                </tr>
                <tr v-for="project in projects" :key="project.id">
                    <td>{{project.nombre}}</td>
                    <td>{{project.fecha1}}</td>
                    <td>{{project.fecha2}}</td>
                    <td>{{project.estatus}}</td>
                    <td>
                        <nuxt-link :to="`/edit/${project.id}`">Editar</nuxt-link>
                    </td>
                    <td>Eliminar</td>
                </tr>
            </table>
        </div>
    </div>
</template>

<script>
    export default {
        layout: 'simple',
        data() {
            return {
                projects: [
                    {id: 0, nombre: 'Proyecto 1', fecha1: '10/03/2020', fecha2: '15/03/2020', estatus: 'activo'},
                    {id: 1, nombre: 'Proyecto 1', fecha1: '10/03/2020', fecha2: '15/03/2020', estatus: 'activo'},
                    {id: 2, nombre: 'Proyecto 1', fecha1: '10/03/2020', fecha2: '15/03/2020', estatus: 'activo'}
                ]
            }
        },
    }
</script>

<style scoped>
.publicaciones{
    height: 75vh;
    background: #FAFAFA;
}
.section{
    padding-left: 0;
    padding-right: 0;
}
.container{
    display: flex;
    justify-content: space-between;
}
.button{
    color: white;
    background: #0584D9;
    border-radius: 8px; 
}
.title{
    font-family: 'Roboto', sans-serif;;
    font-style: normal;
    font-weight: bold;
    font-size: 20px;
    line-height: 27px;
    color: #000000;
}
.table{
    margin-top: 32px;
    border-radius: 12px;
    box-shadow: 4px 7px 7px rgba(0, 0, 0, 0.25);
}
td, th{
    padding-top: 24px;
    padding-bottom: 24px;
}
</style>
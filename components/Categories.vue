<template>
    <div class="container">
        <div v-for="categoria in categorias" :key="categoria.id">
            <button class="categoria button">{{ categoria.nombre }}</button>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Categories',
        data() {
            return {
                categorias: [
                    {id: 0, nombre: 'Todos'},
                    {id: 1, nombre: 'Educación'},
                    {id: 2, nombre: 'Salud y bienestar'},
                    {id: 3, nombre: 'Vivienda'},
                    {id: 4, nombre: 'Emprendimiento social'},
                    {id: 5, nombre: 'Tecnología' },
                    {id: 6, nombre: 'Medio Ambiente' },
                    {id:7, nombre: 'Equidad de género'},
                    {id:8, nombre: 'Derechos humanos'},
                    {id:9, nombre: 'Participación ciudadana'}
                ]
            }
        },
    }
</script>

<style scoped>
.container{
    display: flex;
    padding: 36px 0;
    justify-content: space-evenly;
    margin-left: var(--margin-desktop);
    margin-right: var(--margin-desktop);
}
.categoria{
    color: #676767;
    font-size: 12px;
    border: none;
}
.categoria:hover{
    color: #676767;
    background: #EAEAEA;
}
</style>
<template>
    <div class="filtros">
        <div class="columns">
            <div class="column" v-for="filtro in filtros" :key="filtro.key">
                <Filtro 
                    :label="filtro.label"
                    :opciones="filtro.opciones"
                />
            </div>
        </div>
    </div>
</template>

<script>
    import Filtro from '~/components/Filtro'
    export default {
        name: 'Filters',
        components: {
            Filtro
        },
        data() {
            return {
                filtros: [
                    {key:1, label: 'Tipo de ayuda', opciones: ['Voluntariado', 'Apoyo económica', 'Donación de artículos','Compra / venta de productos']},
                    {key:2, label: 'Organización', opciones: ['Organización 1', 'Organización 2', 'Organización 3']},
                    {key:3, label: 'Ciudad', opciones: ['Monterrey', 'Guadalupe', 'San Nicolás de los Garza']}
                ]
            }
        },
    }
</script>

<style scoped>
.columns{
    margin-left: var(--margin-desktop);
    margin-right: var(--margin-desktop);
}
</style>
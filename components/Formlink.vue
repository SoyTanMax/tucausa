<template>
    <div class="section">
        <p class="pregunta">{{ pregunta }}</p>
        <nuxt-link :to="'/register'" class="button">Llena el formulario</nuxt-link>
    </div>
</template>

<script>
    export default {
        name: 'Formlink',
        data() {
            return {
                pregunta: '¿Buscas publicar tu proyecto o actividad?'
            }
        },
    }
</script>

<style scoped>
.section{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
.pregunta{
    font-weight: bold;
    font-size: 24px;
    color: #484848;
    margin-bottom: 24px;
}
.button{
    background: var(--main-color);
    color: white;
    border-radius: 8px;
    border: none;
    height: 40px;
}
</style>
<template>
    <footer class="footer">
        <nuxt-link :to="'/'">
            <div class="logo"><p class="tu">Tu</p><p class="causa">Causa</p></div>
        </nuxt-link>
        <p class="copy">©2021 Tecnológico de Monterrey. Todos los derechos reservados.</p>
        <p class="text">{{ text }}</p>
    </footer>
</template>

<script>
    export default {
        name: 'Footer',
        data() {
            return {
                text: 'Made with <3 in Mty'
            }
        },
    }
</script>

<style scoped>
.footer{
    padding: 48px var(--margin-desktop);
    background: #FAFAFA;;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
}
.logo{
    display: flex;
    font-family: 'Nunito', sans-serif;
    font-size: 24px;
    font-weight: 700;
}
.tu{
    color: #000000;
}
.copy, .text{
    font-family: 'Nunito', sans-serif;
    font-weight: bold;
    font-size: 16px;
    color: #575757
}
</style>
<template>
    <div class="login">
        <div class="nav">
            <div class="navbar-item is-paddingless">
                <nuxt-link :to="'/'">
                    <div class="logo"><p class="tu">Tu</p><p class="causa">Causa</p></div>
                </nuxt-link>
            </div>
            <p>No estás registrado? <nuxt-link :to="'/register'"> Llena nuestro formulario </nuxt-link> </p>
        </div>
        <div class="image-container">
            <div class="container">
                <p class="publica">{{heroText}}</p>
                <img :src="heroImage" alt="">
            </div>
        </div>
        <div class="component-container column">
            <Login />
        </div>
    </div>
</template>

<script>
    import Login from '~/components/Login'
    export default {
        components: {
            Login
        },
        data() {
            return {
                heroText: 'Publica y comparte tus proyectos como organización.',
                heroImage: require('@/images/sitted.svg'),
            }
        },
    }
</script>

<style scoped>
body{
    margin: 0;
}
.login{
    position: relative;
    display: flex;
}
.nav{
    position: absolute;
    width: 100%;
    top: 0;
    left: 0;
    height: 80px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-left: var(--margin-desktop);
    padding-right: var(--margin-desktop);
    font-family: 'Nunito', sans-serif;
    z-index:  99;
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
.image-container{
    position: relative;
    width: 40%;
    background: #D9F2F8;
    height: 100vh;
    z-index: 98;
    
}
.container{
    margin-left: var(--margin-desktop);
    padding-top: 35%;
}
.publica{
    color: #333333;
    font-family: Roboto;
    font-style: normal;
    font-weight: bold;
    font-size: 28px;
    line-height: 33px;
    width: 380px;
    text-align: left;
}
img{
    max-width: 350px;
    margin-top: 50px;
}
.column{
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
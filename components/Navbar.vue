<template>
    <nav class="navbar is-transparent" :class="{'home': home}">
        <div class="navbar-brand">
            <div class="navbar-item is-paddingless">
                <nuxt-link :to="'/'">
                    <div class="logo"><p class="tu">Tu</p><p class="causa">Causa</p></div>
                </nuxt-link>
            </div>
            <div class="navbar-item">
                <Search />
            </div>
            <div class="navbar-burger" @click="showNav = !showNav" :class="{ 'is-active': showNav }">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </div>
        <div class="navbar-end">
            <div class="navbar-menu" :class="{ 'is-active': showNav }">
                <div class="navbar-start">
                    <ul class="navbar-item" :style="{'padding-right': '0px'}">
                        <nuxt-link :to="'/'">
                            <li class="link">
                                Inicio
                            </li>
                        </nuxt-link>
                        <nuxt-link :to="'/publicaciones'">
                            <li class="link" v-if="loggedIn">
                                Mis publicaciones
                            </li>
                        </nuxt-link>
                        <nuxt-link :to="'/'">
                            <li class="link">
                                Nosotros
                            </li>
                        </nuxt-link>
                        <nuxt-link :to="'/'">
                            <li class="link">
                                Contacto
                            </li>
                        </nuxt-link>
                        <nuxt-link :to="'/login'" class="button" v-if="!loggedIn">
                            Iniciar sesión
                        </nuxt-link>
                    </ul>
                    <div class="account">
                        <img class="profile" src="@/images/orgImage.jpg" alt="" v-if="loggedIn" @click="isActive = !isActive">
                        <div class="options" v-show="isActive">
                            <nuxt-link class="option" :to="'/'">
                                Perfil
                            </nuxt-link>
                            <nuxt-link class="option" :to="'/'">
                                Editar perfil
                            </nuxt-link>
                            <nuxt-link class="option" :to="'/'">
                                Ajustes
                            </nuxt-link>
                            <div class="option" @click="loggedIn = false, isActive = false">
                                Cerrar sesión
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </nav>
</template>

<script>
    import Search from '~/components/Search'
    export default {
        name: 'Navbar',
        props: ['home'],
        components: {
            Search
        },
        data() {
            return {
                showNav: false,
                isActive: false,
                loggedIn: true,
            }
        },
    }
</script>

<style scoped>
.navbar{
    height: 80px;
    padding: 0 96px;
}
.home{
    padding: 0;
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
.link{
    margin-right: 32px;
    font-family: 'Roboto', sans-serif;
    color: #454545;
    font-weight: 500;
    font-size: 16px;
}
.navbar-start{
    display: flex;
    align-items: center;
}
.account{
    position: relative;
}
.profile{
    background-position: center;
    background-size: cover;
    border-radius: 50%;
    width: 50px;
    height: 50px;
}
.options{
    background: white;
    position: absolute;
    left: -200px;
    margin-top: 10px;
    border: 1px solid #d5d5d5;
    border-radius: 8px;
    padding-top: 16px;
    padding-bottom: 16px;
}
.option{
    display: flex;
    width: 100%;
    color: #676767;
    padding-left: 16px;
    padding-top: 6px;
    padding-bottom: 6px;
    margin-right: 150px;
}
.option:hover{
    background: #e9e9e9;
}
.button{
    background: var(--main-color);
    color: white;
    border-radius: 8px;
    border: none;
}
/* Mobile */
@media (max-width: 1024px){
    .navbar{
        height: 52px;
        padding-left: 24px;
        padding-right: 0;
    }
    .home{
        padding: 0;
    }
}
</style>
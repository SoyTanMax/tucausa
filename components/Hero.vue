<template>
    <div class="hero">
        <div class="hero-head">
            <Navbar class="navbar" :home="home"/>
        </div>
        <div class="hero-body">
            <div class="columns is-fullwidth">
                <div class="column is-half is-paddingless">
                    <div class="column-content">
                        <p class="heroText">{{ heroText }}</p>
                    </div>
                </div>
                <div class="column">
                    <img class="heroImage" :src="heroImage" alt="">
                </div>
            </div>
        </div>
        <div class="circle"></div>
    </div>
</template>

<script>
    import Navbar from '~/components/Navbar'
    export default {
        name: 'Hero',
        components: {
            Navbar
        },
        data() {
            return {
                heroText: 'Encuentra tu causa y participa en proyectos de impacto social.',
                heroImage: require('@/images/hero.svg'),
                home: true
            }
        },
    }
</script>

<style scoped>
.hero-body{
    padding-top: 72px;
}
.heroText{
    font-size: 32px;
    font-weight: bold;
    color: #333333;
    line-height: 40px;
    font-family: 'Roboto', sans-serif;
}
.column{
    display: flex;
    align-items: center;
}
.heroImage, .navbar{
    z-index:99;
}
.button{
    background: var(--main-color);
    color: white;
    border: none;
    border-radius: 8px;
    margin-top: 32px;
    font-size: 20px;
    font-family: 'Roboto', sans-serif;
}
svg{
    width: 20px;
    margin-left: 8px;
}
.circle{
    position: absolute;
    background: rgba(5, 132, 217, 0.25);
    position: absolute;
    width: 497px;
    height: 497px;
    left: 50%;
    top: -20%;
    border-radius: 50%;
    z-index: 98;
}
</style>
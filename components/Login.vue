<template>
    <div class="login">
        <p class="ingresa">Ingresa con el usuario proporcionado por Tu Causa.</p>
        <form @submit.prevent>
            <div class="field email">
                <div class="label">Email</div>
                <div class="control">
                    <input type="email" class="input">
                </div>
            </div>
            <div class="field">
                <div class="label">Contraseña</div>
                <div class="control">
                    <input type="password" class="input">
                </div>
            </div>
            <nuxt-link :to="'Recovery'" class="recovery">
                Olvidaste tu contraseña?
            </nuxt-link>
            <button class="button">
                Iniciar sesion
            </button>
        </form>
        
    </div>
</template>

<script>
    export default {
        name: 'Login'
    }
</script>

<style scoped>
.login{
    display: flex;
    font-family: 'Roboto', sans-serif;
    flex-direction: column;
    max-width: 550px;
    justify-content: center;
}
.ingresa{
    margin-bottom: 42px;
    font-family: Roboto;
    font-weight: bold;
    font-size: 18px;
    color: #333333;
}
.button{
    font-family: 'Roboto', sans-serif;
    background: #0584D9;
    border: none;
    border-radius: 8px;
    color: white;
    width: 170px;
}
.input{
    background: #EFEFEF;
}
form{
    max-width: 300px;
}
.email{
    margin-bottom: 26px;
}
.recovery{
    display: flex;
    justify-content: flex-end;
    margin-bottom: 42px;
}
</style>
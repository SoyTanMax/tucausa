<template>
    <div class="registro">
        <div class="background"></div>
        <div class="nav">
            <div class="navbar-item is-paddingless">
                <nuxt-link :to="'/'">
                    <div class="logo"><p class="tu">Tu</p><p class="causa">Causa</p></div>
                </nuxt-link>
            </div>
            <p>Ya estás registrado? <nuxt-link :to="'/login'"> Inicia sesión </nuxt-link></p>
        </div>
        <div class="section">
            <form @submit.prevent>
                <p class="titulo">Formulario de registro</p>
                <div class="box">
                    <div class="title-container">
                        <svg class="w-6 h-6" fill="#646464" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10 2a1 1 0 00-1 1v1a1 1 0 002 0V3a1 1 0 00-1-1zM4 4h3a3 3 0 006 0h3a2 2 0 012 2v9a2 2 0 01-2 2H4a2 2 0 01-2-2V6a2 2 0 012-2zm2.5 7a1.5 1.5 0 100-3 1.5 1.5 0 000 3zm2.45 4a2.5 2.5 0 10-4.9 0h4.9zM12 9a1 1 0 100 2h3a1 1 0 100-2h-3zm-1 4a1 1 0 011-1h2a1 1 0 110 2h-2a1 1 0 01-1-1z" clip-rule="evenodd"></path></svg>                        <p class="section-title">Contacto</p>
                    </div>
                    <div class="columns">
                        <div class="column">
                            <div class="field">
                                <div class="label">Nombre de la persona de contacto</div>
                                <div class="control">
                                    <input type="text" class="input">
                                </div>
                            </div>
                            <div class="field">
                                <div class="label">Telefono celular</div>
                                <div class="control">
                                    <input type="text" class="input">
                                </div>
                            </div>
                        </div>
                        <div class="column">
                            <div class="field">
                                <div class="label">Correo electrónico</div>
                                <div class="control">
                                    <input type="email" class="input">
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="line"></div>
                    <div class="title-container">
                        <svg class="w-6 h-6" fill="#646464" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path d="M13 6a3 3 0 11-6 0 3 3 0 016 0zM18 8a2 2 0 11-4 0 2 2 0 014 0zM14 15a4 4 0 00-8 0v3h8v-3zM6 8a2 2 0 11-4 0 2 2 0 014 0zM16 18v-3a5.972 5.972 0 00-.75-2.906A3.005 3.005 0 0119 15v3h-3zM4.75 12.094A5.973 5.973 0 004 15v3H1v-3a3 3 0 013.75-2.906z"></path></svg>
                        <p class="section-title">Acerca de la organización</p>
                    </div>
                    <div class="columns">
                        <div class="column">
                            <div class="field">
                                <div class="label">Nombre de la organización</div>
                                <div class="control">
                                    <input type="text" class="input">
                                </div>
                            </div>
                            <div class="field">
                                <div class="label">Describe brevemente la actividad principal de tu organización.</div>
                                <div class="control">
                                    <textarea class="textarea" cols="30" rows="6"></textarea>
                                </div>
                            </div>
                            <div class="field">
                                <div class="label">Link a página web o redes sociales</div>
                                <div class="control">
                                    <input type="text" class="input">
                                </div>
                            </div>
                            <div class="field">
                                <div class="label">Correo de contacto a publicarse en el perfil</div>
                                <div class="control">
                                    <input type="email" class="input">
                                </div>
                            </div>
                        </div>
                        <div class="column">
                            <div class="columns">
                                <div class="column">
                                    <div class="field segundo">
                                        <div class="label">Ubicación</div>
                                        <div class="control">
                                            <input type="text" class="input">
                                        </div>
                                    </div>
                                </div>
                                <div class="column">
                                    <div class="field segundo">
                                        <div class="label">Población atendida</div>
                                        <div class="control">
                                            <input type="text" class="input">
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="field">
                                <div class="label">Misión y visión de la organización.</div>
                                <div class="control">
                                    <textarea cols="30" rows="6" class="textarea"></textarea>
                                </div>
                            </div>
                            <div class="field">
                                <div class="label">Logo</div>
                                <input type="file" name="" id="">
                            </div>
                        </div>
                    </div>
                    <div class="button-container">
                        <button class="button">Enviar formulario</button>
                    </div>
                </div>
            </form>
            
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.registro{
    position: relative;
    height: 100%;
    background: #eeeeee;
}
.section{
    z-index: 99;
    position: relative;
    padding: 16px 0;
}
.background{
    position: absolute;
    top: 0;
    left: 0;
    background: #D9F2F8;
    width: 100%;
    height: 30%;
    z-index: 98;
}
.nav{
    position: relative;
    width: 100%;
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
.titulo{
    font-family: Roboto;
    font-style: normal;
    font-weight: bold;
    font-size: 24px;
    line-height: 28px;
    color: #000000;
    margin-bottom: 16px;
}
.box{
    border-radius: 12px;
    padding: 42px;
}
.title-container{
    display: flex;
    align-items: center;
    margin-bottom: 18px;
}
svg{
    width: 24px;
    margin-right: 10px;
}
.section-title{
    font-family: Roboto;
    font-style: normal;
    font-weight: bold;
    font-size: 18px;
    line-height: 21px;
    color: #444444;
    
}
.label{
    font-family: Roboto;
    font-style: normal;
    font-weight: bold;
    font-size: 14px;
    line-height: 16px;
    color: #3D3D3D;
}
.field{
    margin-bottom: 28px;
}
.input, .textarea{
    background: #EFEFEF;
    border-radius: 8px;
}
.segundo{
    margin-bottom: 2px;
}
.button{
    color: white;
    background: #0584D9;
    border-radius: 8px; 
    width: 197px;
    height: 50px;
}
.button-container{
    display: flex;
    justify-content: flex-end;
}
.line{
    width: 100%;
    border-bottom: 1px solid #c7c7c7;
    margin-bottom: 42px;
}
</style>
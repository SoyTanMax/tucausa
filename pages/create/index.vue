<template>
    <div class="create">
        <div class="section">
            <div class="box">
                <form @submit.prevent>
                    <div class="columns">
                        <div class="column">
                            <div class="add-image">
                                <svg class="w-6 h-6" fill="#b4b4b4" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-11a1 1 0 10-2 0v2H7a1 1 0 100 2h2v2a1 1 0 102 0v-2h2a1 1 0 100-2h-2V7z" clip-rule="evenodd"></path></svg>
                                <p>Añade aquí la foto de tu proyecto</p>
                            </div>
                            <div class="columns">
                                <div class="column">
                                    <div class="add-image-small"></div>
                                </div>
                                <div class="column">
                                    <div class="add-image-small"></div>
                                </div>
                                <div class="column">
                                    <div class="add-image-small"></div>
                                </div>
                                <div class="column">
                                    <div class="add-image-small"></div>
                                </div>
                                <div class="column">
                                    <div class="add-image-small"></div>
                                </div>
                            </div>
                        </div>
                        <div class="column">
                            <div class="field">
                                <div class="label">Título del proyecto</div>
                                <div class="control">
                                    <input type="text" class="input">
                                </div>
                            </div>
                            <div class="columns">
                                <div class="column">
                                    <div class="field">
                                        <div class="label">Objetivo de desarrollo sustentable</div>
                                        <div class="control">
                                            <input type="text" class="input">
                                        </div>
                                    </div>
                                    <div class="field">
                                        <div class="label">Necesidad</div>
                                        <div class="control">
                                            <input type="text" class="input">
                                        </div>
                                    </div>
                                </div>
                                <div class="column">
                                    <div class="field">
                                        <div class="label">Causa</div>
                                        <div class="control">
                                            <input type="text" class="input">
                                        </div>
                                    </div>
                                    <div class="field">
                                        <div class="label">Población atendida</div>
                                        <div class="control">
                                            <input type="text" class="input">
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="field">
                                <div class="label">Descripción del proyecto</div>
                                <div class="control">
                                    <textarea name="" id="" cols="30" rows="6" class="textarea"></textarea>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="button-container">
                        <button class="button">Guardar</button>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        layout: 'simple',
        data() {
            return {
            }
        }
    }
</script>

<style scoped>
.section{
    padding-left: 0;
    padding-right: 0;
    height: 100%;
}
.box{
    padding: 52px 42px;
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
.add-image{
    border: 2px dashed #b4b4b4;
    border-radius: 12px;
    width: 100%;
    height: 350px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-bottom: 24px;
}
svg{
    width: 50px;
    margin-bottom: 24px;
}
.add-image-small{
    border: 2px dashed #b4b4b4;
    border-radius: 12px;
    width: 100%;
    height: 80px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.button{
    color: white;
    font-weight: bold;
    background: #0584D9;
    border-radius: 8px; 
    width: 197px;
    height: 50px;
}
.button-container{
    display: flex;
    justify-content: flex-end;
}
</style>
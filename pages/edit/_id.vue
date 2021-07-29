<template>
    <div class="create">
        <div class="section">
            <div class="box">
                <form @submit.prevent>
                    <div class="columns">
                        <div class="column">
                            <img :src="image" alt="" class="project-image">
                            <div class="columns">
                                <div class="column">
                                    <img :src="image" alt="" class="project-image-small">
                                </div>
                                <div class="column">
                                    <img :src="image" alt="" class="project-image-small">
                                </div>
                                <div class="column">
                                    <img :src="image" alt="" class="project-image-small">
                                </div>
                                <div class="column">
                                    <img :src="image" alt="" class="project-image-small">
                                </div>
                                <div class="column">
                                    <img :src="image" alt="" class="project-image-small">
                                </div>
                            </div>
                        </div>
                        <div class="column">
                            <div class="field">
                                <div class="label">Título del proyecto</div>
                                <div class="control">
                                    <input type="text" class="input" v-model="titulo">
                                </div>
                            </div>
                            <div class="columns">
                                <div class="column">
                                    <Select :label="labels[0]" :opciones="objetivos"/>
                                    <Select :label="labels[1]" :opciones="causas"/>
                                </div>
                                <div class="column">
                                    <Select :label="labels[2]" :opciones="necesidades"/>
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
                                    <textarea name="" id="" cols="30" rows="6" class="textarea" v-model="descripcion"></textarea>
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
    import Select from '~/components/Select'
    export default {
        layout: 'simple',
        components:{
            Select
        },
        data() {
            return {
                image: require('@/images/projectImage.jpg'),
                titulo: 'Proyecto 0',
                labels: ['Objetivo de desarrollo sustentable', 'Necesidad', 'Causa'],
                objetivos: ['Objetivo 1', 'Objetivo 2', 'Objetivo 3'],
                causas: ['Causa 1', 'Causa 2', 'Causa 3'],
                necesidades: ['Necesidad 1', 'Necesidad 2', 'Necesidad 3'],
                descripcion: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ullam, eveniet pariatur. Rerum ipsum cupiditate iusto qui soluta quisquam nihil quis voluptatum, unde quas dolorem? Vitae ut minus quas placeat id.Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ullam, eveniet pariatur. Rerum ipsum cupiditate iusto qui soluta quisquam nihil quis voluptatum, unde quas dolorem? Vitae ut minus quas placeat id.'
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
.project-image{
    border-radius: 12px;
    width: 100%;
    height: 350px;
    margin-bottom: 24px;
}
svg{
    width: 50px;
    margin-bottom: 24px;
}
.project-image-small{
    border-radius: 12px;
    width: 100%;
    height: 80px;
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
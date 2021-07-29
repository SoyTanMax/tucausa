<template>
    <div class="proyecto">
        <div class="section">
            <div class="columns">
                <div class="column">
                    <div class="slider">
                        <img class="slider-image" :src="image" alt="">
                    </div>
                </div>
                <div class="column is-1">
                    <img class="org-image" :src="orgImage" alt="">
                </div>
                <div class="column is-half">
                    <p class="titulo">Nombre del proyecto</p>
                    <p class="texto">Publicado por {{ nombre }} el 09 / 03/ 2020</p>
                    <p class="titulo segundo">Descripción</p>
                    <p class="texto">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Natus numquam magni dicta, necessitatibus laboriosam error autem nemo commodi quis minus sequi totam, eaque sunt perferendis beatae doloribus sed rem! Reiciendis?</p>
                    <p class="titulo segundo">Contacto</p>
                    <p class="texto">correoelectrónico@gmail.com</p>
                </div>
            </div>
            
        </div>
        <div class="section">
            <div class="container">
                <div class="columns">
                    <div class="column">
                        <div class="line"></div>
                    </div>
                    <div class="column mid-section is-narrow">
                        <img :src="orgImage" alt="" class="org-image">
                    </div>
                    <div class="column">
                        <div class="line"></div>
                    </div>
                </div>
            </div>
            <div class="container organizacion">
                <p class="titulo">{{ nombre }}</p>
                <nuxt-link :to="`/o/${orgId}`" class="button">Ver más</nuxt-link>
            </div>
        </div>
        <div class="section more">
            <p class="titulo mas">Más de {{ nombre }}</p>
            <div class="container related">
                <div v-for="project in projects" :key="project.id">
                    <Project 
                        :id="project.id"
                        :name="project.name"
                        :image="project.image"
                        :orgName="project.orgName"
                        :orgImage="project.orgImage"
                        :orgId="project.orgId"
                    />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Project from '~/components/Project'
    export default {
        layout: 'simple',
        components:{
            Project
        },
        data() {
            return {
                image: require('@/images/projectImage.jpg'),
                orgImage: require('@/images/orgImage.jpg'),
                nombre: 'Nombre de la organización',
                projects: [
                    {id: 0, name: 'projecto 1', image: require('@/images/projectImage.jpg'), orgName: 'Organización 1', orgImage: require('@/images/orgImage.jpg'), orgId: 0},
                    {id: 1, name: 'projecto 1', image: require('@/images/projectImage.jpg'), orgName: 'Organización 1', orgImage: require('@/images/orgImage.jpg'), orgId: 1},
                    {id: 2, name: 'projecto 1', image: require('@/images/projectImage.jpg'), orgName: 'Organización 1', orgImage: require('@/images/orgImage.jpg'), orgId: 2},
                    {id: 3, name: 'projecto 1', image: require('@/images/projectImage.jpg'), orgName: 'Organización 1', orgImage: require('@/images/orgImage.jpg'), orgId: 3}
                ]
            }
        },
    }
</script>

<style scoped>
.section{
    padding-left: 0;
    padding-right: 0;
}
.titulo{
    font-family: Roboto;
    font-style: normal;
    font-weight: bold;
    font-size: 18px;
    line-height: 21px;
    color: #000000;
    margin-bottom: 8px;
}
.texto{
    font-family: Roboto;
    font-style: normal;
    font-weight: normal;
    font-size: 12px;
    line-height: 14px;
    color: #585858;
    margin-bottom: 24px;
}
.segundo{
    margin-bottom: 16px;
}
.slider-image{
    border-radius: 12px;
}
.org-image{
    width: 50px;
    height: 50px;
    border-radius: 50%;
}
.is-1{
    display: flex;
    justify-content: flex-end;
}
.mid-section{
    display: flex; 
    justify-content: center;
}
.mid-section .org-image{
    width: 70px;
    height: 70px;
}
.line{
    width: 100%;
    height: 50%;
    border-bottom: 1px solid #9E9E9E;
}
.organizacion{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 12px;
}
.button{
    background: var(--main-color);
    color: white;
    border-radius: 8px;
    border: none;
    height: 40px;
    width: 145px;
    margin-top: 24px;
}
.related{
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 15px;
    margin: 0;
}
.more{
    padding-top: 0;
    padding-bottom: 90px;
}
.mas{
    margin-bottom: 24px;
}
</style>
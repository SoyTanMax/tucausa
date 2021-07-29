<template>
    <div class="organización">
        <div class="section">
            <div class="box">
                <div class="columns">
                    <div class="column is-narrow is-2">
                        <img :src="orgImage" alt="" class="org-image">
                    </div>
                    <div class="column is-8">
                        <p class="titulo">Nombre de la organización</p>
                        <p class="texto">Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora illum corporis recusandae doloribus fuga non placeat. Ipsum, obcaecati ex ut labore dolores consequatur in praesentium modi excepturi laborum, id impedit. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dolorem laudantium iusto fugiat eligendi repellat iste tempore odit nam nobis molestiae, eaque vel sequi illo laboriosam, eum eius aliquid incidunt ad.</p>
                        <div class="columns">
                            <div class="column details is-narrow">
                                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd"></path></svg>
                                <p class="texto detail">Ubicación</p>
                            </div>
                            <div class="column details is-narrow">
                                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"></path><path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"></path></svg>
                                <p class="texto detail">Correodecontacto@gamil.com</p>
                            </div>
                            <div class="column details is-narrow">
                                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M4.083 9h1.946c.089-1.546.383-2.97.837-4.118A6.004 6.004 0 004.083 9zM10 2a8 8 0 100 16 8 8 0 000-16zm0 2c-.076 0-.232.032-.465.262-.238.234-.497.623-.737 1.182-.389.907-.673 2.142-.766 3.556h3.936c-.093-1.414-.377-2.649-.766-3.556-.24-.56-.5-.948-.737-1.182C10.232 4.032 10.076 4 10 4zm3.971 5c-.089-1.546-.383-2.97-.837-4.118A6.004 6.004 0 0115.917 9h-1.946zm-2.003 2H8.032c.093 1.414.377 2.649.766 3.556.24.56.5.948.737 1.182.233.23.389.262.465.262.076 0 .232-.032.465-.262.238-.234.498-.623.737-1.182.389-.907.673-2.142.766-3.556zm1.166 4.118c.454-1.147.748-2.572.837-4.118h1.946a6.004 6.004 0 01-2.783 4.118zm-6.268 0C6.412 13.97 6.118 12.546 6.03 11H4.083a6.004 6.004 0 002.783 4.118z" clip-rule="evenodd"></path></svg>
                                <p class="texto detail">paginaweb.com</p>
                            </div>
                        </div>
                    </div>
                    <div class="column"></div>
                </div>
            </div>
        </div>
        <div class="section more">
            <p class="titulo mas">Proyectos de {{ nombre }}</p>
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
    export default {
        layout: 'simple',
        data() {
            return {
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
.box{
    padding: 52px 38px;
    border-radius: 12px;
}
.org-image{
    width: 150px;
    height: 150px;
    border-radius: 50%;
}
.titulo{
    font-family: Roboto;
    font-style: normal;
    font-weight: bold;
    font-size: 18px;
    line-height: 21px;
    color: #000000;
    margin-bottom: 24px;
}
.texto{
    font-family: Roboto;
    font-style: normal;
    font-weight: normal;
    font-size: 12px;
    line-height: 14px;
    color: #585858;
    margin-bottom: 18px;
}
.is-narrow{
    display: flex;
    justify-content: center;
}
svg{
    width: 24px;
    margin-right: 10px
}
.details{
    display: flex;
    align-items: center;
    justify-content: center;
}
.detail{
    margin-bottom: 0;
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
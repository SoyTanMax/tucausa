<template>
    <div class="projects section">
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
</template>

<script>
    import Project from '~/components/Project'
    export default {
        name: 'Projects',
        components: {
            Project
        },
        data() {
            return {
                projects: [
                    {id: 0, name: 'projecto 1', image: require('@/images/projectImage.jpg'), orgName: 'Organización 1', orgImage: require('@/images/orgImage.jpg'), orgId: 0},
                    {id: 1, name: 'projecto 1', image: require('@/images/projectImage.jpg'), orgName: 'Organización 1', orgImage: require('@/images/orgImage.jpg'), orgId: 1},
                    {id: 2, name: 'projecto 1', image: require('@/images/projectImage.jpg'), orgName: 'Organización 1', orgImage: require('@/images/orgImage.jpg'), orgId: 2},
                    {id: 3, name: 'projecto 1', image: require('@/images/projectImage.jpg'), orgName: 'Organización 1', orgImage: require('@/images/orgImage.jpg'), orgId: 3},
                    {id: 4, name: 'projecto 1', image: require('@/images/projectImage.jpg'), orgName: 'Organización 1', orgImage: require('@/images/orgImage.jpg'), orgId: 4},
                    {id: 5, name: 'projecto 1', image: require('@/images/projectImage.jpg'), orgName: 'Organización 1', orgImage: require('@/images/orgImage.jpg'), orgId: 5},
                    {id: 6, name: 'projecto 1', image: require('@/images/projectImage.jpg'), orgName: 'Organización 1', orgImage: require('@/images/orgImage.jpg'), orgId: 6},
                    {id: 7, name: 'projecto 1', image: require('@/images/projectImage.jpg'), orgName: 'Organización 1', orgImage: require('@/images/orgImage.jpg'), orgId: 7}
                ]
            }
        },
    }
</script>

<style scoped>
.projects{
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 15px;
    padding-left: 12px;
    padding-right: 12px;
}
</style>
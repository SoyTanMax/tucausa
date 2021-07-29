<template>
    <div class="project">
        <nuxt-link :to="`/p/${id}`">
            <img class="projectImage" :src="image" alt="">
        </nuxt-link>
        <nuxt-link class="org" :to="`/o/${orgId}`">
            <img class="orgImage" :src="orgImage" alt="">
            <p class="orgName">{{ orgName }}</p>
        </nuxt-link>
    </div>
</template>

<script>
    export default {
        name: 'Project',
        props: ['id','image', 'name', 'orgName', 'orgImage', 'orgId']
    }
</script>

<style scoped>
.projectImage{
    background-position: center;
    background-size: cover;
    border-radius: 8px;
    height: 200px;
}
.org{
    display: flex;
    align-items: center;
}
.orgImage{
    background-position: center;
    background-size: cover;
    border-radius: 50%;
    width: 35px;
    height: 35px;
    margin-right: 8px;
}
.orgName{
    font-weight: bold;
    color: #464646;
}
</style>
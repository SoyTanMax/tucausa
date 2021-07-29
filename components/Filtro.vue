<template>
    <div class="field">
        <div class="container">
            <label for="" class="label">{{ label }}</label>
            <p v-if="filtro != 'Todos'" @click="filtro = 'Todos'" class="limpiar">Limpiar</p>
        </div>
        <button class="button is-fullwidth" @click="isActive = !isActive">
            <p class="predeterminado">{{ filtro }}</p>
            <svg class="w-6 h-6 arrow" :class="{'up': isActive}" fill="#A4A4A4" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
        </button>
        <div class="options" v-show="isActive">
            <div v-for="option in opciones" :key="option.id">
                <div class="option" @click="filter(option)">{{ option }}</div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Filtro',
        props: ['label', 'opciones'],
        data() {
            return {
                isActive: false,
                filtro: 'Todos'
            }
        },
        methods: {
            filter(option){
                this.filtro = option
                this.isActive = false
            }
        }
    }
</script>

<style scoped>
.field{
    position: relative;
}
.button{
    height: 40px;
    border: 1px solid #d5d5d5;
    border-radius: 8px;
    display: flex;
    justify-content: space-between;
}
.predeterminado{
    font-size: 14px;
    color: #A4A4A4
}
.arrow{
    width: 24px;
    transition: 300ms;
}
.up{
    transform: rotate(-180deg);
}
.options{
    position: absolute;
    background: white;
    margin-top: 10px;
    border: 1px solid #d5d5d5;
    border-radius: 8px;
    padding-top: 16px;
    padding-bottom: 16px;
    width: 100%;
}
.option{
    display: flex;
    color: #676767;
    padding-left: 16px;
    padding-top: 6px;
    padding-bottom: 6px;
}
.option:hover{
    background: #e9e9e9;
}
.container{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 8px;
}
.limpiar{
    font-size: 14px;
    color: var(--main-color);
}
.label{
    margin: 0;
}
</style>
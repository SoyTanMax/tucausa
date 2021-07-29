<template>
    <div class="field">
        <p class="control has-icons-left">
            <input type="text" class="input" placeholder="Buscar...">
            <span class="icon is-small is-left">
                <svg class="search w-6 h-6" fill="#8c8c8c" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z" clip-rule="evenodd"></path></svg>
            </span>
        </p>
    </div>
</template>

<script>
    export default {
        name: 'search'
    }
</script>

<style scoped>
.field{
    margin-left: 32px;
}
.input{
    background: #eeeeee;
}
input:focus{
    background: white;
}
.search{
    width: 20px;
}
::placeholder{
    color: #8c8c8c
}
</style>
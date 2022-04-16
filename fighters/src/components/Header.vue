<template>
    <header id="header-component">
        <h1>
            {{title}}
        </h1>
    </header>    
</template>


<script>
    export default ({
        name: 'header-component',

        data() {
            return {
                title: 'Vue Fighters'
            }
        }
    })
</script>


<style scoped>

    #header-component {
        background-color: rgb(131, 30, 30);
        color: whitesmoke;
        padding: 2rem;
    }

</style>
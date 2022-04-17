<template>
    <header id="header-component">
        <h1>
            {{title}}
        </h1>
        <h2 v-on:click="changeTitle">
            {{fightersComponentTitle}}
        </h2>
    </header>    
</template>


<script>
    export default ({
        name: 'header-component',

        props : {
            fightersComponentTitle : {
                type : String
            }
        },

        data() {
            return {
                title: 'Vue Fighters'
            }
        },

        methods : {
            changeTitle() {
                this.fightersComponentTitle = "(Max 3 Fighters)"
            }
        }
    })
</script>


<style scoped>

    #header-component {
        background-color: rgb(131, 30, 30);
        color: whitesmoke;
        padding: 2rem;
        margin:0;
    }

</style>
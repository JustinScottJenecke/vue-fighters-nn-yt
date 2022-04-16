<template>
    <main id="fighters-elem">

        <h2>{{title}}</h2>
        <ul id="fighters-list">
            <li v-for="(fighter, i) in fightersList" :key="i" >
                {{ fighter }}
            </li>
        </ul>

    </main>
</template>


<script>

    export default ({
        name: 'fighters-elem',

        data() {
            return {

                title: 'Select your fighter!',

                fightersList : [
                    'Riyu',
                    'Gene',
                    'Scorpio',
                    'Mia',
                    'Begeta'
                ]
            }
        }
    })

</script>


<style scoped>

    #fighters-elem {
        margin:0;
        background-color: rgb(61, 61, 61);
        color: black;
        padding: 1rem;
        min-height: 76vh;
    }

    #fighters-list {
        list-style: none;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        padding: 1rem;    
    }

    #fighters-list li {
        padding: 1rem;
        margin: 1rem;
        background-color: gray;
    }

</style>
<template>
    <section id="fighters-elem">

        <h2>{{title}}</h2>
        <ul id="fighters-list" v-on:click="test">
            <li 
                class="fighter-card"
                v-for="(fighter, i) in fightersList" 
                :key="i"
                v-on:mouseover="fighter.show = true" v-on:mouseleave="fighter.show = false" 
            >
               <h2> 
                   {{ fighter.name }} 
                </h2>
               <span v-show="fighter.show">
                   Special Move: <b> {{fighter.speciality}} </b>
               </span>
               <button> 
                   {{fighter.show}} 
                </button>
                <button v-on:click="deleteFighter"> 
                   Remove from Team
                </button>
            </li>
        </ul>

    </section>
</template>


<script>

    export default ({
        name: 'fighters-elem',

        // --- props ---
        props:{
                // list of fighter objects
                fightersList:{
                    type : Array,
                    required : true
                }
            },

        // --- local data ---
        data() {
            return {

                title: 'Team Battle: Select your fighter!',

            }
        },

        // --- methods ---
        methods : {
            test() {
                console.log(this.fightersList)
            },
            deleteFighter() {
                this.fightersList.pop()
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
        margin: 1rem; 
    }

    .fighter-card {
        flex-grow: 1;
        background-color: gray;
        display: flex;
        flex-direction: column;
        padding: 5rem;
        border: solid 1rem rgb(61, 61, 61);;
    }

    #fighters-list li * {
        margin: 0.5rem 0;
    }

</style>
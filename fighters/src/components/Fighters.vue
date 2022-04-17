<template>
    <section id="fighters-elem">

        <h2>{{title}}</h2>
        <ul id="fighters-list">
            <li 
                class="fighter-card"
                v-for="(fighter, i) in fightersList" 
                :key="i"
                v-on:click="fighter.show = !fighter.show" 
            >
               <h2> 
                   {{ fighter.name }} 
                </h2>
               <span>
                   Special Move: <b> {{fighter.speciality}} </b>
               </span>
               <button> 
                   {{fighter.show}} 
                </button>
            </li>
        </ul>

    </section>
</template>


<script>

    export default ({
        name: 'fighters-elem',

        data() {
            return {

                title: 'Select your fighter!',

                fightersList : [
                    {name:'Riyu', speciality: 'hadoken', show: false},
                    {name:'Gene', speciality: 'dorya', show: false},
                    {name:'Scorpio', speciality: 'spear', show: false},
                    {name:'Mia', speciality: 'Chou Hissatsu Shinobi-Bachi', show: false},
                    {name:'Begeta', speciality: 'galick gun', show: false}
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
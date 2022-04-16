<template>
    <div id="fighters">
        <ul>
            <li v-for="(fighter, index) in fightersList" :key="index">
                {{ fighter }}
            </li>
        </ul>
    </div>
</template>

<script>
export default ({
    name: 'FightersComponent',
    
    data() {
        return {
            fightersList: ["Riyu", "Gene", "Begeta", "Scorpio", "Chung-Lee"] 
        }
    }
    
})
</script>

<style scoped>
    #fighters {
        display: flex;
        flex-direction: column;
        margin: 0 40vw;
        text-align: left;

        color: rgb(143, 143, 143);
    }

    #fighters ul {
        list-style: none;
    }
</style>

<template>
  <div id="app">

    <header-component 
      v-bind:fightersComponentTitle="fightersComponentTitle" 
    />

    <fighters-component  
      v-bind:fightersComponentTitle="fightersComponentTitle"
      v-bind:fightersList="fightersList"
    />

    <footer-component
      v-bind:fightersComponentTitle="fightersComponentTitle"
      v-on:footerTitleChange="updateTitle($event)"
    />

  </div>
</template>


<script>
import Header from './components/Header.vue';
import Footer from './components/FooterComponent.vue';
import Fighters from './components/Fighters.vue';


  export default {
  
    name: "app",

    // ----- Data -----
    data() {
      return {
        
        fightersList : [
            {name:'Riyu', speciality: 'Hadoken', show: false},
            {name:'Gene', speciality: 'Dorya', show: false},
            {name:'Scorpio', speciality: 'Spear', show: false},
            {name:'Mia', speciality: 'Chou Hissatsu Shinobi-Bachi', show: false},
            {name:'Begeta', speciality: 'Galick gun', show: false}
        ],

        fightersComponentTitle: "Team Battle:"
      }
    },

    // ----- Components -----
    components: {
      'header-component': Header,
      'footer-component': Footer,
      'fighters-component': Fighters
    },

    // ----- Methods -----
    methods : {

      updateTitle(args) {
        this.fightersComponentTitle = args
      }
      
    }
  }

</script>


<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin: 0;
  }

  #app * {
    margin: 0;
  }
</style>

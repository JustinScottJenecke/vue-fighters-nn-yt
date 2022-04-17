<template>
  <div id="app">

    <header-component/>

    <fighters-component v-bind:fightersList="fightersList"/>

    <footer-component/>

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
        ]        
      }
    },
    // ----- Components -----
    components: {
      'header-component': Header,
      'footer-component': Footer,
      'fighters-component': Fighters
    }

  }
        Header
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

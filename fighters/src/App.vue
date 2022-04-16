<template>
  <div id="app">

    <header-component/>

    <fighters-component/>

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

<template>
  <div id="app">

    <header-component/>
    
    <main>
      Hello Fighters!
    </main>

    <footer-component/>

  </div>
</template>


<script>
import Header from './components/Header.vue';
import Footer from './components/FooterComponent.vue';


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
      'footer-component': Footer
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
</style>

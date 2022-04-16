<template>
  <div id="app">
    <h1> {{ title }} </h1>
    <p>
      {{ paraOne }}
    </p>
    <fighters/>
  </div>
</template>


<script>
  import Fighters from "./components/Fighters.vue";

  export default {
  
    name: "app",

    // ----- Data -----
    data() {
      return {
        title: 'Fighters App',
        paraOne: "The World's Warriors"
      }
    },
    // ----- Components -----
    components: { 
      Fighters 
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
    margin-top: 60px;
  }
</style>

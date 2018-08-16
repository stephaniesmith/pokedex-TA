<template>
  <div id="app">
    <Header/>
    <Results :pokemonList="pokemon"/>
  </div>
</template>

<script>
import pokemon from './assets/pokemon.js';
import Header from './components/Header.vue';
import Results from './components/Results.vue';

export default {
  name: 'app',
  components: {
    Header,
    Results
  },
  data() {
    return { pokemon };
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  margin-top: 60px;
}
</style>

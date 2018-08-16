<template>
  <div id="app">
    <Header :types="types"/>
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
  },
  computed: {
    types() {
      const typeOne = this.pokemon.map(p => p.type_1);
      const typeTwo = this.pokemon.map(p => p.type_2);
      const set = new Set(typeOne.concat(typeTwo));
      return [...set.values()];
    }
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
}
</style>

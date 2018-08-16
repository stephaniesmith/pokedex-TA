<template>
  <div id="app">
    <Header :filter="filter" :types="types"/>
    <Results :list="list"/>
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
    return { 
      pokemon,
      filter: {
        type: 'all'
      }
    }
  },
  computed: {
    filtered() {
      const { type } = this.filter;
      return this.pokemon.filter(p => type === 'all' || p.type_1 === type || p.type_2 === type)
    },
    list() {
      console.log(this.filtered);
      return this.filtered;
    },
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

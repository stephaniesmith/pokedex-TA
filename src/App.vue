<template>
  <div id="app">
    <Header :sort="sort" :filter="filter" :types="types"/>
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
      sort: {
        props: 'id'
      },
      filter: {
        type: 'all'
      }
    };
  },
  computed: {
    filtered() {
      const { type } = this.filter;
      return this.pokemon.filter(p => type === 'all' || p.type_1 === type || p.type_2 === type);
    },
    list() {
      const { props } = this.sort;
      return this.filtered.sort((a, b) => {
        const propA = a[props];
        const propB = b[props];
        if(propA > propB) return 1;
        if(propA < propB) return -1;
        return 0;
      });
    },
    types() {
      const typeOne = this.pokemon.map(p => p.type_1);
      const typeTwo = this.pokemon.map(p => p.type_2);
      const set = new Set(typeOne.concat(typeTwo));
      return [...set.values()];
    }
  }
};
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

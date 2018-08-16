<template>
  <div id="results">
    <h1>Results</h1>
    <div id="pokemon-list">
      <Tile
        v-for="pokemon in list"
        :key="pokemon.pokemon"
        :pokemon="pokemon"
      />
    </div>
  </div>
</template>

<script>
  import Tile from './Tile.vue';
  export default {
    props: ['list'],
    components: {
      Tile
    }
    
  }
</script>

<style scoped>
  #results {
    background-color: cadetblue;
  }

  #pokemon-list {
    margin: 0 3em;
    display: grid;
    grid-gap: 2em;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  }
</style>
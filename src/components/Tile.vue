<template>
  <div id="pokemon" :style="{ backgroundImage: 'url(' + pokemon.url_image + ')' }">
    <h2>{{pokemon.pokemon.toUpperCase()}}</h2>
    <div class="stats">
      <h3>Type: {{pokemon.type_1}}</h3>
      <h3>Attack: {{pokemon.attack}}</h3>
      <h3>Defense: {{pokemon.defense}}</h3>
    </div>
  </div>
</template>

<script>
export default {
  props: ['pokemon']
};
</script>

<style>
  #pokemon {
    background-color: rgb(230, 228, 228);
    background-position: center;
    background-repeat: none;
    background-size: cover;
    min-height: 300px;
    border: 15px solid rgba(0, 0, 0, .4);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .stats {
    margin: 1.5em;
    background-color: rgba(0, 0, 0, .4);
    padding: .5em 1em;
    width: fit-content;
  }

  #pokemon h2 {
    margin-top: .5em;
    font-size: 2em;
    font-weight: bold;
    filter: drop-shadow(10px 5px 5px black)
  }

  #pokemon h3 {
    text-align: left;
    font-weight: bold;
    font-size: 1.25em;
    line-height: 1.5em;

  }
</style>
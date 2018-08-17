<template>
  <div id="pokemon" :style="{ backgroundImage: 'url(' + pokemon.url_image + ')' }">
    <h2>{{pokemon.pokemon}}</h2>
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
  }
</script>

<style>
  #pokemon {
    background-position: center;
    background-repeat: none;
    background-size: cover;
    min-height: 300px;
    border: 15px solid white;
    padding: 1.5em;
    display: flex;
    flex-direction: column;
    justify-content: space-between
  }

  .stats {
    background-color: rgba(0, 0, 0, .4);
    padding: .5em 1em;
    width: fit-content;
  }

  #pokemon h2 {
    font-size: 2.5em;
    font-weight: bold;
    filter: drop-shadow(10px 5px 5px black)
  }

  #pokemon h3 {
    text-align: left;
    font-weight: bold;
    font-size: 1.25em;
    line-height: 1.5em;

  }
</style>s
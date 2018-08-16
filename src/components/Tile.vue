<template>
  <div id="pokemon" :style="{ backgroundImage: 'url(' + pokemon.url_image + ')' }">
    <h2>{{pokemon.pokemon}}</h2>
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
  }
</style>
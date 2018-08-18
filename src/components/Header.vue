<template>
  <header id="header">
    <h1>Pokédex</h1>
    <div class="sort-filter">
      <Filters :filter="filter" :types="types"/>
      <Sort :sort="sort"/>
    </div>
  </header>
</template>

<script>
import Filters from './Filters.vue';
import Sort from './Sort.vue';

export default {
  components: {
    Filters,
    Sort
  },
  props: ['types', 'filter', 'sort']
};
</script>

<style scoped>
  #header {
    background-color: rgb(235, 0, 0);
    height: 100px;
  }

  #header h1 {
    padding-top: .5em;
    font-size: 2.5em;
    font-weight: bolder;
  }

  .sort-filter {
    display: flex;
    justify-content: center;
    width: 100vw;
  }
</style>
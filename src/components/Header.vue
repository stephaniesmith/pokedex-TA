<template>
  <header id="header">
    <h1>Header</h1>
    <Filters :filter="filter" :types="types"/>
    <Sort :sort="sort"/>
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
  }
</script>

<style scoped>
  #header {
    background-color: cornflowerblue;
    height: 100px;
  }
</style>
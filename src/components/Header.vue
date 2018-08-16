<template>
  <header id="header">
    <h1>Header</h1>
    <Filters :filter="filter" :types="types"/>
    <Sort/>
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
    props: ['types', 'filter']
  }
</script>

<style scoped>
  #header {
    background-color: cornflowerblue;
    height: 100px;
  }
</style>
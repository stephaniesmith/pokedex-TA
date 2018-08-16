<template>
  <header id="header">
    <h1>Header</h1>
    <Filters :types="types"/>
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
    props: ['types']
  }
</script>

<style scoped>
  #header {
    background-color: cornflowerblue;
    height: 100px;
  }
</style>
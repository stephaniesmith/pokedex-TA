<template>
  <header id="header">
    <h1>Header</h1>
    <Filters/>
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
    }
  }
</script>

<style scoped>
  #header {
    background-color: cornflowerblue
  }
</style>
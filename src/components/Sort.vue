<template>
  <select v-model="sort.props">
      <option value="id">Sort</option>
      <option value="pokemon">name</option>
      <option value="type_1">type</option>
      <option value="attack">attack</option>
      <option value="defense">defence</option>
    </select>
</template>

<script>
export default {
  props: ['sort']
};
</script>

<style scoped>
  select {
    background-color: white;
    border: none;
    margin: .5em;
    padding: .5em;
  }
</style>
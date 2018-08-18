<template>
    <select v-model="filter.type">
      <option value="all">
        All types
      </option>
      <option v-for="type in types" :key="type">
        {{ type }}
      </option>
    </select>
</template>

<script>
export default {
  props: ['types', 'filter']
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
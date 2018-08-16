<template>
    <select>
      <option>All types</option>
      <option v-for="type in types"
        :key="type"
      >
        {{ type }}
      </option>
    </select>
</template>

<script>
  export default {
    
    props: ['types']
  }
</script>

<style scoped>

  select {
    background-color: white;
    border: none;
  }

</style>
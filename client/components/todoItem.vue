<template>
  <li>
    <p>{{ todo.copy }}</p>
    <input
      type="checkbox"
      v-model="todo.completed"
      />
  </li>
</template>

<script>
  export default {
    data () {
      return {}
    },
    props: ['todo']
  }
</script>

<style scoped>
  li {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border: 1px solid #000;
    width: 20em;
    height: 2em;
    margin-bottom: 2%;
    padding: 0 1%;
  }
</style>

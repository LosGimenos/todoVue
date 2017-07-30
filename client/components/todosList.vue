<template>
  <ul>
    <todo-item
      v-for="todo in todos"
      v-bind:todo="todo">
    </todo-item>
  </ul>
</template>

<script>
  import TodoItem from './todoItem.vue';

  export default {
    data () {
      return {}
    },
    components: { TodoItem },
    props: ['todos']
  }
</script>

<style scoped>
  ul {
    margin-top: 5%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 90%;
    min-height: min-content;
    list-style: none;
  }
</style>

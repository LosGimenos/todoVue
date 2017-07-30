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
    list-style: none;
  }
</style>

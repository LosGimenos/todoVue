<template>
  <div class="input-panel">
    <h2>Enter the task!</h2>
    <input-bar
      v-bind:todoText="todoText"
      v-on:todoText="value => updateValue(value)"
      v-bind:addTodo="addTodo">
    </input-bar>
  </div>
</template>

<script>
  import InputBar from './inputBar.vue';

  export default {
    data () {
      return {
        panelTodoText: this.todoText
      }
    },
    components: { InputBar },
    props: ['addTodo', 'todoText'],
    methods: {
      updateValue(value) {
        this.panelTodoText = value
        this.$emit('todoText', this.panelTodoText);
      }
    }
  }
</script>

<style scoped>
  .input-panel {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border: 1px solid #000;
    width: 40%;
    height: 10em;
  }
</style>


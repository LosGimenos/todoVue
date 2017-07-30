<template>
  <div>
    <title-bar></title-bar>
    <div class="main-content__wrapper">
      <input-panel
        v-bind:todoText="todoText"
        v-on:todoText="value => todoText = value"
        v-bind:addTodo="addTodo">
      </input-panel>
      <todos-panel
        v-bind:todos="todos">
      </todos-panel>
    </div>
  </div>
</template>

<script>
  import TitleBar from './titleBar.vue';
  import InputPanel from './inputPanel.vue';
  import TodosPanel from './todosPanel.vue';

  export default {
    data () {
      return {
        todoText: '',
        todos: [
          {
            copy: 'Grab a burger',
          },
          {
            copy: 'Frolic in forest',
          }
        ]
      }
    },
    components: {
      TitleBar,
      InputPanel,
      TodosPanel
    },
    methods: {
      addTodo(e) {
        const todoText = this.todoText.trim();
        if (todoText) {
          this.todos.push({
            copy: todoText,
            completed: false,
            isEditing: false
          });
        this.todoText = '';
        }
      }
    }
  }
</script>

<style>
  * {
    margin: 0 0;
  }
  .main-content__wrapper {
    display: flex;
    justify-content: space-around;
  }
</style>

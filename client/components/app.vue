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
            completed: false,
            isEditing: false
          },
          {
            copy: 'Frolic in forest',
            completed: false,
            isEditing: false
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
      addTodo() {
        const todoText = this.todoText.trim();
        if (todoText) {
          this.todos.push({
            copy: todoText,
            completed: false,
            isEditing: false
          });
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

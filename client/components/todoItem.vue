<template>
  <li v-bind:class="{completed: isCompleted}">
    <p
      v-on:click="clickHandler"
      v-show="!isEditing">
      {{ todo.copy }}
    </p>
    <input
      v-show="isEditing"
      v-model="todo.copy"
      v-on:keyup.enter="setValue"
    />
    <input
      type="checkbox"
      v-model="isCompleted"
    />
  </li>
</template>

<script>
  export default {
    data () {
      return {
        isEditing: false,
        isCompleted: false,
      }
    },
    props: ['todo'],
    methods: {
      clickHandler() {
        this.isEditing = true;
      },
      setValue() {
        this.isEditing = false;
      }
    }
  }
</script>

<style scoped>
  li {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border: 1px solid #000;
    width: 20em;
    min-height: 2em;
    margin-bottom: 2%;
    padding: 0 1%;
  }

  .completed {
  background-color: #EC644B;
  text-decoration: line-through;
  }

  li input:focus {
    outline: 0;
  }
</style>

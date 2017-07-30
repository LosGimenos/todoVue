<template>
  <input
    ref="input"
    v-bind:todoText="todoText"
    @input="updateValue"
    v-on:keyup.enter="addTodo"
    placeholder="What do you need to do?" />
</template>

<script>
  export default {
    data () {
      return {}
    },
    props: ['addTodo', 'todoText'],
    methods: {
      updateValue() {
        this.$emit('todoText', this.$refs.input.value)
      }
    }
  }
</script>

<style scoped>
  input {
    width: 60%;
    height: 2em;
    font-size: 1.25em;
    margin-top: 2%;
  }
</style>

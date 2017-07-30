<template>
  <input
    ref="input"
    v-model="inputText"
    @input="updateValue"
    v-on:keyup.enter="submitHandler"
    placeholder="What do you need to do?" />
</template>

<script>
  export default {
    data () {
      return {
        inputText: this.todoText
      }
    },
    props: ['addTodo', 'todoText'],
    methods: {
      updateValue() {
        this.$emit('todoText', this.$refs.input.value)
      },
      submitHandler(e) {
        e.preventDefault();
        this.addTodo();
        this.inputText = '';
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

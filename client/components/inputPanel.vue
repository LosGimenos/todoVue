<template>
  <div class="input-panel">
    <h2>Enter the task!</h2>
    <input-bar></input-bar>
  </div>
</template>

<script>
  import InputBar from './inputBar.vue';

  export default {
    data () {
      return {}
    },
    components: { InputBar }
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


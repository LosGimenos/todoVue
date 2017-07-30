<template>
  <div class="todos-panel">
    <h2>Your Tasks!</h2>
    <todos-list
      v-bind:todos="todos">
    </todos-list>
  </div>
</template>

<script>
  import TodosList from './todosList.vue';

  export default {
    data () {
      return {}
    },
    components: { TodosList },
    props: ['todos']
  }
</script>

<style scoped>
  .todos-panel {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    border: 1px solid #000;
    width: 50%;
    height: 80vh;
    overflow-y: auto;
  }

  .todos-panel h2 {
    position: fixed;
    text-align: center;
    background-color: #fff;
    width: 45%;
  }
</style>

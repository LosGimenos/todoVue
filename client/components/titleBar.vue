<template>
  <div class="title"><h1>{{ title }}</h1></div>
</template>

<script>
  export default {
    data () {
      return {
        title: "That's How VUE...toDO!!"
      }
    }
  }
</script>

<style scoped>
  .title {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #D2D7D3;
    color: #F62459;
    text-align: center;
    height: 15vh;
  }
</style>

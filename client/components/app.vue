<template>
  <div>
    <title-bar></title-bar>
    <input-panel></input-panel>
  </div>
</template>

<script>
  import TitleBar from './titleBar.vue';
  import InputPanel from './inputPanel.vue';

  export default {
    data () {
      return {}
    },
    components: {
      TitleBar,
      InputPanel
    }
  }
</script>

<style>
  * {
    margin: 0 0;
  }
</style>

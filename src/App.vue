<template>
  <div id="app">
    <GraphComponent msg="Welcome to Graph Library" />
  </div>
</template>

<script>
import GraphComponent from './components/GraphComponent.vue'

export default {
  name: 'App',
  components: {
    GraphComponent
  }
}
</script>

<style>
#app {
}
</style>

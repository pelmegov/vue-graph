<template>
  <div class="graph">
    <h1>{{ msg }}</h1>
    <v-stage ref="stage" :config="stageSize">
      <VertexComponent />
      <VertexComponent :x-position="200" :y-position="200" />
      <VertexComponent :x-position="300" :y-position="300" />
      <VertexComponent :x-position="400" :y-position="400" />
      <VertexComponent :x-position="200" :y-position="400" />
      <VertexComponent :x-position="300" :y-position="500" />
    </v-stage>
  </div>
</template>

<script>
import VertexComponent from './VertexComponent'

const width = window.innerWidth
const height = window.innerHeight

export default {
  name: 'GraphComponent',
  components: {
    VertexComponent
  },
  props: {
    msg: {
      type: String,
      default: ''
    }
  },
  data: function () {
    return {
      stageSize: {
        width: width,
        height: height
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

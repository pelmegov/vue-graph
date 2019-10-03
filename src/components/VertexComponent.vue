<template>
  <v-layer ref="layer">
    <v-circle
      :config="{
        x: xPosition,
        y: yPosition,
        radius: 50,
        draggable: true,
        shadowBlur: 5,
        fill: isDragging ? '#00C851' : '#007E33'
      }"
      @dragstart="handleDragStart"
      @dragend="handleDragEnd"
    />
  </v-layer>
</template>

<script>
export default {
  name: 'VertexComponent',
  props: {
    xPosition: {
      type: Number,
      default: 100
    },
    yPosition: {
      type: Number,
      default: 100
    }
  },
  data () {
    return {
      isDragging: false
    }
  },
  methods: {
    handleDragStart () {
      this.isDragging = true
    },
    handleDragEnd () {
      this.isDragging = false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

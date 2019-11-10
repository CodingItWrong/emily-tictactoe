<template>
  <button class="square" @click="cycleShape">{{ this.shape }}</button>
</template>

<script>
const shapes = ['_', 'X', 'O']

export default {
  name: 'Square',
  data() {
    return {
      shapeIndex: 0,
    }
  },
  computed: {
    shape() {
      return shapes[this.shapeIndex]
    },
  },
  methods: {
    cycleShape() {
      this.shapeIndex = (this.shapeIndex + 1) % 3
    },
  },
}
</script>

<style scoped>
.square {
  display: inline;
  border: solid 1px black;
  font-size: 72px;
}
</style>

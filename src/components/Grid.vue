<template>
  <div>
    <div>{{turnShape}}'s turn</div>
    <div v-for="(row, rowIndex) in rows" :key="rowIndex">
      <Square
        v-for="(space, columnIndex) in row"
        :key="columnIndex"
        :shape="shapes[space]"
        :row="rowIndex"
        :column="columnIndex"
        @toggle-shape="handleToggle"
      />
    </div>
  </div>
</template>

<script>
import Vue from 'vue'
import Square from './Square'

export default {
  name: 'Grid',
  components: { Square },
  data() {
    return {
      rows: [
        [0, 0, 0],
        [0, 0, 0],
        [0, 0, 0],
      ],
      shapes: ['_', 'X', 'O'],
      turn: 1,
    }
  },
  methods: {
    handleToggle({ row, column }) {
      const newValue = this.turn

      Vue.set(this.rows[row], column, newValue)

      this.turn = this.turn === 1 ? 2 : 1
    },
  },
  computed: {
    shape(shapeIndex) {
      return this.shapes[shapeIndex]
    },
    turnShape() {
      return this.shapes[this.turn]
    },
  },
}
</script>

<style>
</style>

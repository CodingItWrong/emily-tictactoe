<template>
  <div>
    <div v-for="(row, index) in rows" :key="index">
      <Square v-for="(space, index) in row" :key="index" :shape="space" />
    </div>
  </div>
</template>

<script>
import Square from './Square'

export default {
  name: 'Grid',
  components: { Square },
  data() {
    return {
      rows: [
        ['X', 'O', 'X'],
        ['_', '_', '_'],
        ['_', '_', '_'],
      ],
    }
  },
}
</script>

<style>
</style>
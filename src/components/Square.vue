<template>
  <button class="square" @click="handleClick">{{ this.shape }}</button>
</template>

<script>
export default {
  name: 'Square',
  props: ['shape', 'row', 'column'],
  methods: {
    handleClick() {
      this.$emit('toggle-shape', {
        row: this.row,
        column: this.column,
      })
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

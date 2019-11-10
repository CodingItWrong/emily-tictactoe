<template>
  <button class="square" @click="cycleShape">{{ this.shape }}</button>
</template>

<script>
export default {
  name: 'Square',
  props: ['shape'],
  methods: {
    cycleShape() {},
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

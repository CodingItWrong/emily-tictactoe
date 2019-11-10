<template>
  <div>
    <div>
      <Square />
      <Square />
      <Square />
    </div>

    <div>
      <Square />
      <Square />
      <Square />
    </div>

    <div>
      <Square />
      <Square />
      <Square />
    </div>
  </div>
</template>

<script>
import Square from './Square'

export default {
  name: 'Grid',
  components: { Square },
}
</script>

<style>
</style>
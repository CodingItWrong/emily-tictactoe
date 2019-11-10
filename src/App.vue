<template>
  <div>
    <h1>The Best Tic-Tac-Toe Ever</h1>
    <h2>Made By Emily</h2>

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
import Square from './components/Square'

export default {
  name: 'app',
  components: { Square },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

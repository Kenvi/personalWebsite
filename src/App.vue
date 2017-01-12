<template>
  <div id="app">
    <img src="./assets/logo.png">
    <winter></winter>
  </div>
</template>

<script>
import Winter from './components/Winter'

export default {
  name: 'app',
  components: {
    Winter
  }
}
</script>

<style lang="less">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  img {
    height: auto;
    width: auto;
  }
}
</style>

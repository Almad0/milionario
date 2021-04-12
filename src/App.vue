<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <MillionComponent/>
  </div>
</template>

<script>
import MillionComponent from "./components/MillionComponent"

export default {
  name: 'App',
  components: {
    MillionComponent
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  img{
    width: 500px;
  }
}
</style>

<template>
  <div id="app">
    <div class="up_div">
      <img alt="Vue logo" src="./assets/logo.png">
    </div>
    <div class="down_div">
      <MillionComponent/>
    </div>
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
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  height:100vh;
  font-family: Avenir, Helvetica, Arial, sans-serif;

  .up_div{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 300px;
    background-color: #0E118E;
    img{
      padding: 20px;
      width: 250px;
    }
  }
  .down_div{
    height: calc(100vh - 300px);
    background-color: #11093A;
  }
}
</style>

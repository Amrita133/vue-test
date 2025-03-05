<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Test-third/>
  </div>
</template>

<script>
import TestThird from './components/Test-third.vue'



export default {
  name: 'App',
  components: {
TestThird

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

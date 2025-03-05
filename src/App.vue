<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <test-fourth/>
  </div>
</template>

<script>
import TestFourth from './components/Test-fourth.vue'

export default {
  name: 'App',
  components: {
     TestFourth

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

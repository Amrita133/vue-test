<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <test-eight/>
  </div>
</template>

<script>
import TestEight from './components/Test-eight.vue';
export default {
  name: 'App',
  components: {
    TestEight
  

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

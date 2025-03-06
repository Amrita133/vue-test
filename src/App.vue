<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <TestFirst/> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <FirstCode/> -->

    <assignment-second/>
  </div>
</template>

<script>
import AssignmentSecond from './components/AssignmentSecond.vue'

// import FirstCode from './components/FirstCode.vue'
// import TestFirst from './components/TestFirst.vue'

export default {
  name: 'App',
  components: {
    AssignmentSecond
    // TestFirst,
    // FirstCode,

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

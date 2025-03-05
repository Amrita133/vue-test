<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <TestFirst/> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <FirstCode/> -->


    <Test-first/>
  </div>
</template>

<script>
// import TestFirstVue from './components/TestFirst.vue'

// import FirstCode from './components/FirstCode.vue'
// import TestFirst from './components/TestFirst.vue'
import TestFirst from './components/Test-first.vue'

export default {
  name: 'App',
  components: {
    // TestFirst,
    // FirstCode,
    TestFirst

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

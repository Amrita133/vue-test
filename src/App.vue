<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
 
 <list-data/>
  </div>
</template>

<script>

import ListData from './components/ListData.vue';

export default {
  name: 'App',
  components: {
   ListData
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

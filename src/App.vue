<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
   <card-c/>
  </div>
</template>

<script>
import CardC from './components/Card-C.vue'
export default {
  name: 'App',
  components: {
 CardC

  }
}
</script>

<style>
#app{
  margin-top: 100px;
  font-family:Arial, Helvetica, sans-serif;
}
</style>

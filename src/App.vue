<template>
  <div id="app">
 <Recipes />
  </div>
</template>

<script>
import Recipes from './components/CallSmart.vue'

export default {
  name: 'App',
  components: {
    Recipes
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

<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <RecepieItem/>
    <RecepieItem/>
    <RecepieItem/>
  </div>
</template>

<script>
import RecepieItem from './components/RecepieItem.vue'

export default {
  name: 'App',
  components: {
    RecepieItem
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

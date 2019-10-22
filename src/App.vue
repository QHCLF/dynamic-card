<template>
  <div id="app">
    <card msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import card from './components/card.vue'

export default {
  name: 'app',
  components: {
    card
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

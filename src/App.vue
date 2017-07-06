<template>
  <div id="app">
    <SuperHeader></SuperHeader>
  </div>
</template>

<script>
import SuperHeader from './components/Header'

export default {
  name: 'app',
  components: {
    SuperHeader
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>

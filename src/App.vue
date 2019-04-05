<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <ComponentA message="Hello Vuejs"/>
    <ComponentB message="Hello Vuejs"/>
    <ComponentC message="Hello Vuejs"/>
  </div>
</template>

<script>
import ComponentA from './components/ComponentA'
import ComponentB from './components/ComponentB'
import ComponentC from './components/ComponentC'

export default {
  name: 'app',
  components: {
    ComponentA,
    ComponentB,
    ComponentC
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
  margin-top: 60px;
}
</style>

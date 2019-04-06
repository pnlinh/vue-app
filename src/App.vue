<template>
  <div id="container">
    <meta name="viewport" content="width=device-width, initial-scale=1">
<!--    <img alt="Vue logo" src="./assets/logo.png">-->
    <PostComponent message="List posts"/>
  </div>
</template>

<script>
// import ComponentA from './components/ComponentA'
// import ComponentB from './components/ComponentB'
// import ComponentC from './components/ComponentC'
import PostComponent from './components/PostComponent'

export default {
  name: 'app',
  components: {
    // ComponentA,
    // ComponentB,
    // ComponentC,
    PostComponent
  }
}
</script>

<style>
</style>

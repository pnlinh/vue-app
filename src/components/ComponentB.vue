<template>
  <div class="hello">
    <h1>{{ message }}</h1>
  </div>
</template>

<script>
export default {
  name: 'ComponentB',
  props: {
    message: String
  }
}
</script>

<style scoped>
h1{
  color: green;
}
</style>

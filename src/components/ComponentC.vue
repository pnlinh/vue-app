<template>
  <div class="hello">
    <h1>{{ message }}</h1>
  </div>
</template>

<script>
export default {
  name: 'ComponentC',
  props: {
    message: String
  }
}
</script>

<style scoped>
h1{
  color: blue;
}
</style>

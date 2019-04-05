<template>
  <div class="hello">
    <h1>{{ message }}</h1>
  </div>
</template>

<script>
export default {
  name: 'ComponentA',
  props: {
    message: String
  }
}
</script>

<style scoped>
h1{
  color: red;
}
</style>

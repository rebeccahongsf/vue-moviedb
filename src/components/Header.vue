<template>
  <header>
    <h1><router-link to="/">{{title}}</router-link></h1>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
    title: String,
  }
}
</script>

<style scoped>
header {
  background: #809B8E;
  padding: 20px;
  color: white;
}

h1 {
  margin: 0;
}

a {
  text-decoration: none;
  color: inherit;
}
</style>
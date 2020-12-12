<template>
  <div id="app">
    <Header :title="title" />
    <MoviesList />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import MoviesList from './components/MoviesList.vue'

export default {
  name: 'App',
  data() {
    return {
      title: "Vue Movie DB",
      isTrue: false,
    }
  },
  components: {
    Header,
    MoviesList,
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

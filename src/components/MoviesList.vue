<template>
  <ul>
    <li v-for="movie in movies" :key="movie.id">
      <Movie :movie="movie" />
    </li>
  </ul>
</template>

<script>
  import Movie from './Movie'

  export default {
    name: "MoviesList",
    data() {
      return {
        movies: []
      }
    },
    created: function() {
      this.fetchData();
    },
    methods: {
      fetchData: async function() {
        try {
          const res = await fetch('https://api.themoviedb.org/3/discover/movie?api_key=500892bdb8989fc3ae5765f1838aa9e1&language=en-US&sort_by=popularity.desc&include_adult=false');
          const movies = await res.json();
          this.movies = movies.results;
        } catch(e) {
          console.lof(e)
        }
      }
    },
    components: {
      Movie,
    }
  }
</script>

<style lang="css" scoped>
  ul {
    list-style: none;
    padding: 1rem;
    margin: 0;
    display: grid;
    grid-row-gap: 1rem;
    grid-template-columns: repeat(6, 1fr);
  }
</style>
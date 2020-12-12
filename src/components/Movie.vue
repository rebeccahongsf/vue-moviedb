<template>
    <img :src="posterImage" :alt="movie.title" />
</template>

<script>
  const POSTER_PATH = "http://image.tmdb.org/t/p/w154";
  export default {
    name: 'Movie',
    props: ['movie'],
    computed: {
      posterImage: function() {
        return `${POSTER_PATH}/${this.movie.poster_path}`;
      }
    }
  }
</script>

<style lang="css" scoped>
  img {
    box-shadow: 0 0 35px #000;
  }
</style>
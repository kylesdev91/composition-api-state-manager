<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <MovieList />
  Number of Movies: {{ numberOfMovies }}
</template>

<script>
import useMovieState from './store/useMovieState';
import MovieList from './MovieList.vue';
export default {
  name: 'App',
  components: {
    MovieList,
  },
  setup: () => {
    const { state: movieState } = useMovieState();
    return {
      numberOfMovies: movieState.movies.length,
    };
  },
};
</script>

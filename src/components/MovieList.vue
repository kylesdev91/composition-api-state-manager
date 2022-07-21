<template>
  <ul>
    <li v-for="movie in movies" :key="movie.id">{{ movie.title }}</li>
  </ul>
</template>

<script>
import useMovieState from '../store/useMovieState';

export default {
  name: 'MovieList',
  setup: () => {
    const { state: movieState } = useMovieState();
    return {
      movies: movieState.movies,
    };
  },
};
</script>

<style></style>

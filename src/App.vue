<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <UserLogin />
  <MovieList />
  Number of Movies: {{ numberOfMovies }}
</template>

<script>
import useMovieState from './store/useMovieState';
import MovieList from './components/MovieList.vue';
import UserLogin from './components/UserLogin.vue';
export default {
  name: 'App',
  components: {
    MovieList,
    UserLogin,
  },
  setup: () => {
    const { getNumberOfMovies } = useMovieState();
    return {
      numberOfMovies: getNumberOfMovies(),
    };
  },
};
</script>

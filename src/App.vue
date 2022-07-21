<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <MovieList />
</template>

<script>
import MovieList from './MovieList.vue';
export default {
  name: 'App',
  components: {
    MovieList,
  },
};
</script>

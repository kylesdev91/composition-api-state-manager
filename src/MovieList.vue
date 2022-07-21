<template>
  <ul>
    <li v-for="movie in movies" :key="movie.id">{{ movie.title }}</li>
  </ul>
</template>

<script>
export default {
  name: 'MovieList',
  setup: () => {
    const movies = [
      {
        id: 1,
        title: 'Movie 1',
      },
      {
        id: 2,
        title: 'Movie 2',
      },
      {
        id: 3,
        title: 'Movie 3',
      },
    ];
    return {
      movies,
    };
  },
};
</script>

<style></style>

<script>
import { store } from "../store";
import SearchBar from "./SearchBar.vue";
export default {
  name: "AppHeader",
  components: {
    SearchBar,
  },
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <h1>
    <ul>
      <li v-for="movie in store.movies">{{ movie.title }}</li>
    </ul>
    <SearchBar />
  </h1>
</template>

<style lang="scss" scoped></style>

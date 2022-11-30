<script>
import { store } from "./store";
import axios from "axios";
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import SearchBar from "./components/SearchBar.vue";

export default {
  components: {
    AppHeader,
    SearchBar,
    AppMain,
  },
  data() {
    return {
      store,
    };
  },
  created() {
    axios
      .get("https://api.themoviedb.org/3/search/movie", {
        params: {
          api_key: "96206fe9368a1ea12d46c2da62d78e08",
          query: "",
          language: "it-IT",
        },
      })
      .then((res) => {
        this.store.movies = res.data.results;
      });
  },
};
</script>

<template>
  <AppHeader />
  <AppMain />
  <SearchBar />
</template>

<style lang="scss">
@import "./style/global.scss";
</style>

<script>
import { store } from "../store.js";
import "/node_modules/flag-icons/css/flag-icons.min.css";

export default {
  name: "SectionMovie",
  data() {
    return {
      store,
    };
  },
  methods: {
    getFlag(lang) {
      if (lang === "en") {
        return "gb";
      } else if (lang === "ko") {
        return "kr";
      } else return lang;
    },
  },
};
</script>

<template>
  <ul>
    <li v-for="movie in store.movies">
      <img
        :src="`https://image.tmdb.org/t/p/w342${movie.poster_path} `"
        alt=""
      />
      <h3>{{ movie.title }}</h3>
      <div v-if="movie.title != movie.original_title">
        {{ movie.original_title }}
      </div>
      <span :class="`fi fi-${getFlag(movie.original_language)}`"></span>
      <div>{{ movie.vote_average }}</div>
    </li>
  </ul>
</template>

<style lang="scss"></style>

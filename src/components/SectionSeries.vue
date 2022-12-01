<script>
import { store } from "../store.js";
import "/node_modules/flag-icons/css/flag-icons.min.css";

export default {
  name: "SectionSeries",
  data() {
    return {
      store,
    };
  },
  methods: {
    getFlag(lang) {
      if (lang === "en") {
        return "gb";
      } else if (string === "ko") {
        return "kr";
      } else return string;
    },
  },
};
</script>

<template>
  <div class="container">
    <ul>
      <li v-for="serie in store.series">
        <img
          :src="`https://image.tmdb.org/t/p/w342${serie.poster_path} `"
          alt=""
        />
        <div>{{ serie.name }}</div>
        <div v-if="serie.name != serie.original_name">
          {{ serie.original_name }}
        </div>
        <span :class="`fi fi-${getFlag(serie.original_language)}`"></span>
        <div>{{ serie.vote_average }}</div>
      </li>
    </ul>
  </div>
</template>

<style lang="scss"></style>

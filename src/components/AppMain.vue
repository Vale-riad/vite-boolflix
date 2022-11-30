<script>
import { store } from "../store";
import AppCard from "./AppCard.vue";
export default {
  name: "AppMain",
  components: {
    AppCard,
  },
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <h1>Main</h1>
  <AppCard />
</template>

<style lang="scss" scoped></style>

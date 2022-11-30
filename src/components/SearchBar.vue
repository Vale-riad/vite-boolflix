<script>
import { store } from "../store";
export default {
  name: "SeachBar",
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <input type="text" placeholder="Scegli un film o una serie tv" />
  <button type="submit">Cerca</button>
</template>

<style lang="scss" scoped></style>

<script>
import SectionMovie from "../components/SectionMovie.vue";
import SectionSeries from "../components/SectionSeries.vue";

export default {
  name: "AppMain",
  components: {
    SectionMovie,
    SectionSeries,
  },
};
</script>

<template>
  <h2>Film</h2>
  <SectionMovie />
  <h2>SERIE</h2>
  <SectionSeries />
</template>

<style lang="scss" scoped>
img {
  max-width: 100%;
}
</style>

<template>
    <div class="mainr">
      <div class="movies">
        <h2>Lista Film</h2>
      <Moviecard v-for="(element, index) in myMovies" :key="index" :details="element" />
      </div>

      <div class="series">
        <h2>Lista SerieTV</h2>
      <Seriecard v-for="(element, index) in mySeries" :key="index" :details="element" />
      </div>
        
    </div>
</template>

<script>
import Moviecard from "../components/Moviecard.vue";
import Seriecard from "../components/Seriecard.vue";

export default {
  name: "Main",
  components: {
  Moviecard,
  Seriecard
},
  props: {
    myMovies: Array,
    mySeries: Array
  },
};
</script>
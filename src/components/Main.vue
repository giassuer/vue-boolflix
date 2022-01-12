<template>
    <div class="mainr">
      <Moviecard v-for="(element, index) in myMovies" :key="index" :details="element" />
        
    </div>
</template>

<script>
import Moviecard from "../components/Moviecard.vue";

export default {
  name: "Main",
  components: {
  Moviecard
},
  props: {
    myMovies: Array
  },
};
</script>
<template>
    <div class="main">
      <h2 class="title-list">Lista Film</h2>
      <div class="titles-container">
      <Moviecard v-for="(element, index) in myMovies" :key="index" :details="element" />
      </div>

      <h2 class="title-list">Lista SerieTV</h2>
      <div class="titles-container">
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

  data: function(){
    return{
      flag: ''
    }
  },

  methods: {
        
    }
};
</script>

<style lang="scss">
@import '../style/general.scss';
</style>
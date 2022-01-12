<template>
    <div class="mainr">
      <Moviecard v-for="(element, index) in myMovies" :key="index" />
        <!-- <ul>
            <li v-for="(element, index) in myMovies" :key="index">
                {{ element.title }}
            </li>
        </ul> -->
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
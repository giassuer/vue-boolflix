<template>
    <div class="movie-card">
        <ul>
            <li v-if="details.backdrop_path != null">
                <img :src="'http://image.tmdb.org/t/p/w500/' + details.backdrop_path" alt="">
            </li>
            <li v-else>
                {{'image not found'}}
            </li>
            <li>
                {{ details.title }}
            </li>
            <li>
                {{ details.original_title }}
            </li>
            <li v-if="details.original_language === 'it' || details.original_language === 'en'">
                <img class="flag" :src="require('../assets/img/' + details.original_language + '.png')" alt="">
            </li>
            <li v-else>
                {{details.original_language}}
            </li>
            <li>
                {{ transformVote() }}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  name: "Moviecard",
  props: {
    details: Object
  },

  data: function(){
      return{
          vote: []
      }
  },

  methods: {
      transformVote: function(){
        let newVote = Math.floor(this.details.vote_average);
        if (newVote > 5) {
            newVote = 5
        }else{
            newVote === newVote
        }
        this.vote.push(newVote)
        return newVote
      }
    }
};
</script>
<template>
    <div class="movie-card">
        <ul>
            <li>
                {{ details.title }}
            </li>
            <li>
                {{ details.original_title }}
            </li>
            <li v-if="details.original_language === 'it' || details.original_language === 'en'">
                <img :src="require('../assets/img/' + details.original_language + '.png')" alt="">
            </li>
            <li v-else>
                {{details.original_language}}
            </li>
            <li>
                {{ details.vote_average }}
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
          flags: ''
      }
  },

  methods: {
        getFlagName: function(){
           
        }
    }
};
</script>
<template>
    <div class="cards-container">
        <ul>
            <li v-if="details.backdrop_path != null">
                <div class="img-container">
                    <img :src="'http://image.tmdb.org/t/p/w342/' + details.backdrop_path" alt="">
                </div> 
            </li>
            <li v-else>
                <div class="img-container">
                    <img src="../assets/img/image-not-found.jpg" alt="">
                </div>
            </li>
            <div class="list-container">
                <li>
                    Titolo: {{ details.title ? details.title : details.name }}
                </li>
                <li>
                     Titolo originale:  {{ details.original_title ? details.original_title : details.original_name }}
                </li>
                <li v-if="details.original_language === 'it' || details.original_language === 'en'">
                    Lingua <img class="flag" :src="require('../assets/img/' + details.original_language + '.png')" alt="">
                </li>
                <li v-else>
                    Lingua {{details.original_language}}
                </li>
                <li>
                    <div class="star" v-for="n in 5" :key="n">
                        <div class="star" v-if="n <= transformVote()">
                            <i class="fas fa-star"></i>
                        </div>
                        <div class="star" v-else>
                            <i class="far fa-star"></i>
                        </div>
                    </div>  
                </li>
                <li>
                    {{details.overview}}
                </li>
            </div>
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
          
      }
  },

  methods: {
      transformVote: function(){
          let newVoto = Math.ceil(this.details.vote_average / 2)

          return newVoto  
      },

    }
};
</script>
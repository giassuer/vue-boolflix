<template>
  <div id="app">
    
    <Header @eventoCustom='getUserFilm'/>

    <Main :myMovies="filmList" />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import axios from 'axios';

export default {
  name: "App",
  components: {
    Header,
    Main
  },

  data: function() {
        return {
          filmList: [],
          searchQuery:''
        };
    },

    methods: {
      /*
       Dalla search bar, al click del button -> emit del valore inserito
       Passi il valore a getFilm (o te lo salvi in altra variabile)
      */
      getFilm: function(){
        console.log('Funziona')
        axios.get('https://api.themoviedb.org/3/search/movie',{
        params: {
          api_key: 'f62d7c222a2b0cbf1cc5ebd58556c2c4',
          query:this.searchQuery
        }
        })
        .then((response) => {
           this.filmList = response.data.results;
           console.log(this.filmList);
        });
      },
      getUserFilm: function(query){
        this.searchQuery = query
        this.getFilm()
      }
    }

};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

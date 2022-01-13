<template>
    <div class="header">
        <div class="logo">
            <img src="../assets/img/netflix-logo.jpg" alt="">
        </div>
        <div class="search">
            <input v-model="userFilm" type="search" name="" id="">
            <button @click="$emit('eventoCustom',userFilm)">search</button>
        </div>
    </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    
  },
  data: function() {
        return {
          userFilm: ''
        };
    },

    methods: {
        
    }
};
</script>

<style lang="scss">
@import '../style/general.scss';
// #app {
//   font-family: Avenir, Helvetica, Arial, sans-serif;
//   -webkit-font-smoothing: antialiased;
//   -moz-osx-font-smoothing: grayscale;
//   text-align: center;
//   color: #2c3e50;
//   margin-top: 60px;
// }

</style>
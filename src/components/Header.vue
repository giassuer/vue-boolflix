<template>
    <div class="header">
        <div class="logo">
            <img src="../assets/img/netflix-logo.jpg" alt="">
        </div>
        <div class="search">
            <input class="search-barr" v-model="userFilm" type="search" name="" id="">
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
</style>
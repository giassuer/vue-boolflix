<template>
    <div class="header">
        <div class="search">
            <input v-model="userFilm" type="search" name="" id="">
            <button @click="$emit('eventoCustom'),getUserFilm()">search</button>
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
        getUserFilm: function() {
            let newUserFilm
            if (this.userFilm.length > 0) {
                newUserFilm = this.userFilm
            }
            return newUserFilm
        }
    }
};
</script>
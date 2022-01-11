<template>
    <div class="header">
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
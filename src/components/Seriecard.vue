<template>
    <div class="series-card">
        <ul>
            <li>
                {{ details.name }}
            </li>
            <li>
                {{ details.original_name }}
            </li>
            <li v-if="details.original_language === 'it' || details.original_language === 'en'">
                <img :src="require('../assets/img/' + details.original_language + '.png')" alt="">
            </li>
            <li>
                {{ details.vote_average }}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  name: "Seriecard",
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
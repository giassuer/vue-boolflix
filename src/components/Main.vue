<template>
    <div class="mainr">
        <ul>
            <li v-for="(element, index) in myMovies" :key="index">
                {{ element.title }}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  name: "Main",
  props: {
    myMovies: Array
  },
};
</script>
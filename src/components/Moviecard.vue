<template>
    <div class="movie-card">
        <ul>
            <li>
                {{ details.title }}
            </li>
            <li>
                {{ details.original_title }}
            </li>
            <li>
                {{ details.original_language }}
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
};
</script>
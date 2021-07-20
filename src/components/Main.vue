<template>
  <div class="main row justify-content-center">

    <Card class="col-4" v-for="film in films" :key="film.id" 
    :title="film.title"
    :date="film.release_date"
    :originalLanguage="film.original_language"
    :vote="film.vote_average"
    :image="film.poster_path"
    />

  </div>
</template>

<script>
import Card from "../components/Card.vue";

export default {
  name: 'Main',

  components: {
    Card,
  },

  methods: {

  },

  props: {
    films: Array,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
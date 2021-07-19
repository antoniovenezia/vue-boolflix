<template>
  <div class="main">

    <Card v-for="film in films" :key="film.id" 
    :title="film.title"
    :date="film.release_date"
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

  props: {
    films: Array,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
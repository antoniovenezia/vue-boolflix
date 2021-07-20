<template>
  <div id="app">
    <Header @search="searchFilm"/>
    <Main class="main" :films="filmsFiltered"/>
  </div>
</template>

<script>
import axios from 'axios';
import Header from "./components/Header.vue";
import Main from "./components/Main.vue"

export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  data() {
    return{
      popular: [],
      filmsFiltered: [],
      }
  },
  created() {
      axios.get('https://api.themoviedb.org/3/movie/popular?api_key=8bdc9f673b987154606c7ccf367b5a13')
        .then((result) => {
            this.popular = result.data.results;
            this.filmsFiltered = result.data.results;
            // console.log(this.films)
        });
  }, 
  methods: {
    searchFilm (searchString) {
      if(searchString.length == 0) {
        this.filmsFiltered = this.popular
        return;
        }
          axios.get(`https://api.themoviedb.org/3/search/multi?api_key=8bdc9f673b987154606c7ccf367b5a13&query=${searchString}`)
          .then((result) => {
          this.filmsFiltered = result.data.results;
          })
        
    }
  },

}
</script>

<style lang="scss">

</style>

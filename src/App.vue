<template>
  <div id="app">
    <Header />
    <Main class="container" :films="films"/>
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
      films: [],
       }
  },
  created() {
      axios.get('https://api.themoviedb.org/3/search/movie?api_key=8bdc9f673b987154606c7ccf367b5a13&query=ritorno+al+futuro')
        .then((result) => {
            this.films = result.data.results
            // console.log(this.films)
        });
    }, 
}
</script>

<style lang="scss">
// #app {
  
// }
</style>

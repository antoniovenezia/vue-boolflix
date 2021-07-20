<template>
  <div class="card row">

    <img class="img-card" :src="`https://image.tmdb.org/t/p/w342/${image}`" alt="">
    <div class="card-description fw-bold text-center">
      <div>Titolo: {{title}}</div>
      <div>Data uscita: {{date}}</div>
      <div>Lingua originale: 
        <img :src="flagLanguage(originalLanguage)" alt="" class="">
      </div>
      <div>Voto: {{vote}}</div>
    </div>

  </div>
</template>

<script>

export default {
  name: 'Card',
  props: {
    img: String,
    title: String,
    date: String,
    originalLanguage: String,
    vote: String,
    image: String
  },
  methods: {
    flagLanguage(originalLanguage) {
    return "./flags/" + originalLanguage + ".png"
    // return require("../assets/flags/" + originalLanguage + ".png") ---Questa è la versione utilizzando "require"
    }
  },
}
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
// img:hover{
//   opacity: 0.6;
// }
.card {
  width: calc(100% / 3);
  // img{
    // width: 100%;
  // }
  .card-description{
    // width: 100%;
    margin-top: 250px;
    position: absolute;
    color: white;
    display: none;
      img{
        width: 25px;
      }
    }
  &:hover
    .card-description{
    display: block;
    }
    
}

</style>
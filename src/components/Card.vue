<template>
  <div class="card row">

    <div class="col">
      <img src="https://image.tmdb.org/t/p/w342/hQq8xZe5uLjFzSBt4LanNP7SQjl.jpg" alt="">
      {{title}}
      {{date}}
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
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
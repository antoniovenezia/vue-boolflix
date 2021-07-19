<template>
  <div class="header">
    <img src="https://serietvconcept.files.wordpress.com/2021/05/netflix.png?w=1024" alt="">
    <input type="text" placeholder="Search">
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.header{
  background-color: black;
  img{
    height: 75px;
  }
  input{
    // margin: 10px;
    position: absolute;
    right: 35px;
    top: 35px;
    // height: 80px;
}
}

</style>

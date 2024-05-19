<template>
  <div class="app-container">
    <div class="products-container">
      <h1 id="container-title">{{ title }}</h1>
      <a id="add-button" href=""><i>+</i>Adicionar</a>
      <h1 id="index-number">
        <a href="">21<i>itens</i></a>
      </h1>
      <h1 id="index-number">
        <a href="">5<i>alocados</i></a>
      </h1>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
export default {
    name: "TotalProducts",
    props:{
        title:String,
    }
}
</script>
    
  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    @import '../css/Styles.scss';
</style>
    
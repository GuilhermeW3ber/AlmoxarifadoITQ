<template>
  <div class="products-container">
    <h1 id="title">{{ title }}</h1>
    <div class="product-buttons-container">
      <a id="base-button" href="">Monitores</a>
      <a id="base-button" href="">TVs</a>
      <a id="base-button" href="">Computadores</a>
      <a id="base-button" href="">Impressoras</a>
      <a id="base-button" href="">Projetores</a>
    </div>
  </div>
  <div class="products-items-container">
    <div class="items-container">
      <div class="item-card">
        <div class="more-container">
          <a id="container-more-button" href=""><i>+</i></a>
        </div>
        <h1 id="card-title">Lenovo H1</h1>
        <h2 id="card-subtitle">Alocado: Templo, Sala 2</h2>
        <h2 id="card-subtitle">Nº De Série: Templo, Sala 2</h2>
        <a id="base-category" href="">Computador</a>
      </div>
    </div>
    <div class="items-container">
      <div class="item-card">
        <div class="more-container">
          <a id="container-more-button" href=""><i>+</i></a>
        </div>
        <h1 id="card-title">Lenovo H1</h1>
        <h2 id="card-subtitle">Alocado: Templo, Sala 2</h2>
        <h2 id="card-subtitle">Nº De Série: Templo, Sala 2</h2>
        <a id="base-category" href="">Computador</a>
      </div>
    </div>
    <div class="items-container">
      <div class="item-card">
        <div class="more-container">
          <a id="container-more-button" href=""><i>+</i></a>
        </div>
        <h1 id="card-title">Lenovo H1</h1>
        <h2 id="card-subtitle">Alocado: Templo, Sala 2</h2>
        <h2 id="card-subtitle">Nº De Série: Templo, Sala 2</h2>
        <a id="base-category" href="">Computador</a>
      </div>
    </div>
    <div class="items-container">
      <div class="item-card">
        <div class="more-container">
          <a id="container-more-button" href=""><i>+</i></a>
        </div>
        <h1 id="card-title">Lenovo H1</h1>
        <h2 id="card-subtitle">Alocado: Templo, Sala 2</h2>
        <h2 id="card-subtitle">Nº De Série: Templo, Sala 2</h2>
        <a id="base-category" href="">Computador</a>
      </div>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
export default {
    name: "ProductHomeList",
    props:{
        title:String,
    }
  }
</script>
      
    <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    @import '../../css/Styles.scss';
</style>
      
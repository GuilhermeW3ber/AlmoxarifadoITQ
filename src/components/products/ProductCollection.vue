<template>
  <div class="collection-container">
    <div class="collection-item">
      <a id="add-button" href=""><i>-</i>Editar</a>
      <h1 id="colection-title">Lenovo H1</h1>
      <p id="notes">Nº De Série: Templo, Sala 2</p>
      <p id="notes">Alocado: Templo, Sala 2</p>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
export default {
    name: "ProductCollection",
    props:{
        title:String,
    }
}
</script>
        
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    @import '../../css/Styles.scss';
</style>
        
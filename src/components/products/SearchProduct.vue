<template>
  <div class="collection-container">
    <div class="collection-search">
      <!-- <a id="add-button" href=""><i>-</i>Editar</a> -->
      <input type="text" placeholder="Buscar" />
    </div>
  </div>
</template>

<script>
/* eslint-disable */
  export default {
      name: "SearchProduct",
      props:{
          title:String,
      }
  }
  </script>
          
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
      @import '../../css/Styles.scss';
  </style>
          
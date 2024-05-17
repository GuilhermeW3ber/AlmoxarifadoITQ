<template>
  <div id="nav">
    <!-- <div class="logo">
      <img src="../assets/logoAgora.png" alt="" />
    </div> -->
    <router-link to="/">Home</router-link>
    <router-link to="/product">Estoque</router-link>
  </div>
</template>

<script>
/* eslint-disable */
export default {
  name: "Navbar",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import '../css/Styles.scss';
  @import '../css/NavbarStyles.scss';
</style>

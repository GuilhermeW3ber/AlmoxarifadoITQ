<template>
  <div>
    <Navbar />
    <router-view />
  </div>
</template>

<script>
/* eslint-disable */
import Navbar from "./components/Navbar.vue";

export default {
  components: {
    Navbar,
  },
};
</script>

<style>
  @import './css/Styles.scss';
</style>

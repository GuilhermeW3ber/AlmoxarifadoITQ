<template>
  <div>
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <TotalProducts title="Almoxarifado" />
    <ProductHomeList title="Produtos Novos" />
    <ProductHomeList title="Últimos Alocados" />
    <Footer />
  </div>
</template>

<script>
/* eslint-disable */
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import TotalProducts from "@/components/TotalProducts.vue";
import Footer from "@/components/Footer.vue";
import ProductHomeList from "@/components/products/ProductHomeList.vue"

export default {
  name: "HomeView",
  components: {
    HelloWorld,
    TotalProducts,
    ProductHomeList,
    Footer
  },
};
</script>

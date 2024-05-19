<template>
  <TotalProducts title="Estoque total" />
  <SearchProduct />
  <ProductCollection />
  <ProductCollection />
  <ProductCollection />
  <Footer />
</template>

<script>
/* eslint-disable */
import HelloWorld from "@/components/HelloWorld.vue";
import TotalProducts from "@/components/TotalProducts.vue";
import Footer from "@/components/Footer.vue";
import ProductHomeList from "@/components/products/ProductHomeList.vue"
import ProductCollection from "@/components/products/ProductCollection.vue"
import SearchProduct from "@/components/products/SearchProduct.vue"

export default {
  name: "ProductView",
  components: {
    HelloWorld,
    SearchProduct,
    TotalProducts,
    ProductHomeList,
    ProductCollection,
    Footer
  },
};
</script>

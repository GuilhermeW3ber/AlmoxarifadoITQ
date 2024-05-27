<template>
  <TotalProducts title="Estoque total" />
  <SearchProduct />
  <ProductCollection />
  <Footer />
</template>

<script>
/* eslint-disable */
import TotalProducts from "@/components/TotalProducts.vue";
import Footer from "@/components/Footer.vue";
import ProductCollection from "@/components/products/ProductCollection.vue"
import SearchProduct from "@/components/products/SearchProduct.vue"

export default {
  name: "ProductView",
  components: {
    SearchProduct,
    TotalProducts,
    ProductCollection,
    Footer
  },
};
</script>

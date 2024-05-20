<template>
  <div>
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <AddProduct />
    <Footer />
  </div>
</template>

<script>
/* eslint-disable */
  // @ is an alias to /src
  import Footer from "@/components/Footer.vue";
  import AddProduct from "@/components/products/addProduct/AddForm.vue";
  
  export default {
    name: "AddProductView",
    components: {
        AddProduct,
        Footer
    },
  };
  </script>
  
<template>
  <div class="collection-table">
    <div class="">
      <div
        class="collection-item"
        v-for="product in products"
        :key="product.id"
      >
        <div>
          <button class="delete-btn" @click="deleteProduct(product.id)">
            -
          </button>
        </div>
        <div id="collection-title">{{ product.models }}</div>
        <div id="highlight">{{ product.type }} {{ product.brand }}</div>
        <div id="notes">ID: {{ product.id }}</div>
        <div id="notes">Nº de Série: {{ product.serials }}</div>
        <div id="notes">Local: {{ product.locations }}</div>
        <div>
          <select
            name="status"
            class="status"
            @change="updateProduct($event, product.id)"
          >
            <option
              :value="s.tipo"
              v-for="s in status"
              :key="s.id"
              :selected="product.status == s.tipo"
            >
              {{ s.tipo }}
            </option>
          </select>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
export default {
    name: "ProductCollection",
    data(){
      return{
        products:null,
        products_id:null,
        status:[],
      }
    },
    methods: {
      async getProducts(){
        const req = await fetch("http://localhost:3000/products");
        const data = await req.json();
        this.products = data;
        console.log(data);
      },
       async getStatus() {

        const req = await fetch('http://localhost:3000/status')

        const data = await req.json()

        this.status = data;

      },
      async deleteProduct(id){
        const req = await fetch(`http://localhost:3000/products/${id}`,{
          method: "DELETE"
        }); 

        const res = await req.json();
        
        this.getProducts();
      }
    },
    mounted(){
      this.getProducts();
      this.getStatus();
    }
}
</script>
        
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    @import '../../css/Styles.scss';
</style>
        
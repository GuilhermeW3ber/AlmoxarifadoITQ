<template>
  <div class="form-container">
    <h1 id="container-title">Cadastro de Produto</h1>
    <Message :msg="msg" v-show="msg" />
    <form @submit="createProduct">
      <div class="input-container">
        <label for="brand">Marca:</label>
        <select name="brand" id="brand" v-model="brand">
          <option value="">Selecione a Marca do Produto</option>
          <option v-for="brand in brands" :key="brand.id" :value="brand.tipo">
            {{ brand.tipo }}
          </option>
        </select>
      </div>
      <div class="input-container">
        <label for="type">Categoria:</label>
        <select name="type" id="type" v-model="type">
          <option value="">Selecione a Categoria do Produto</option>
          <option v-for="type in types" :key="type.id" :value="type.tipo">
            {{ type.tipo }}
          </option>
        </select>
      </div>
      <div class="input-container">
        <label for="model">Modelo:</label>
        <input
          type="text"
          id="model"
          name="model"
          v-model="model"
          placeholder="Modelo do Produto"
        />
      </div>
      <div class="input-container">
        <label for="serial">Número de Série:</label>
        <input
          type="text"
          id="serial"
          name="serial"
          v-model="serial"
          placeholder="Nº de Série"
        />
      </div>
      <div class="input-container">
        <label for="location">Localização:</label>
        <select name="location" id="location" v-model="location">
          <option value="">Selecione a Categoria do Produto</option>
          <option
            v-for="location in locations"
            :key="location.id"
            :value="location.tipo"
          >
            {{ location.tipo }}
          </option>
        </select>
      </div>
      <div class="input-container">
        <input type="submit" class="submit-button" value="Adicionar" />
      </div>
    </form>
  </div>
</template>

<script>
/* eslint-disable */
import Message from "../Message.vue";
    export default {
        name: "AddForm",
        data(){
          return{
            brands:null,
            brand:null,
            types:null,
            type:null,
            information:[],
            msg:null,
            models: null,
            locations:null,
            location:null,
            serials:null,
          }
        },
        methods:{
          async getProductInfos(){
            const req = await fetch("http://localhost:3000/productInfos")
            const data=await req.json();

            this.brands = data.brands;
            this.types = data.types;
            this.locations = data.locations;
            this.serials = data.serials;

            console.log(data.products);
          },

          async createProduct(e){
            e.preventDefault();

            // console.log("Produto Criado");

            const data={
              brand: this.brand,
              type: this.type,
              models: this.model,
              locations: this.location,
              serials: this.serial,
              status: "Disponível",
            };

            console.log(data);

            const dataJson = JSON.stringify(data);
            const req = await fetch("http://localhost:3000/products", {
              method:"POST",
              headers: {"Content-Type": "application/json"},
              body:dataJson
            });

            const res = await req.json();
            console.log(res);

            this.msg = `Produto ID ${res.id} registrado com socesso!`

          }
        },
        mounted(){
          this.getProductInfos();
        },
        components:{
          Message
        }
    }
    </script>
            
    <!-- Add "scoped" attribute to limit CSS to this component only -->
    <style scoped>
        @import '../../../css/Styles.scss';
    </style>
            
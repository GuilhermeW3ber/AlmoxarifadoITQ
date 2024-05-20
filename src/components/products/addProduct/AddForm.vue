<template>
  <div class="form-container">
    <h1 id="container-title">Cadastro de Produto</h1>
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
      <label for="name">Modelo:</label>
      <input
        type="text"
        id="name"
        name="name"
        v-model="name"
        placeholder="Nome do Produto"
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
      <input
        type="text"
        id="location"
        name="location"
        v-model="location"
        placeholder="Localização"
      />
    </div>
    <div class="input-container">
      <input type="submit" class="submit-button" value="create" />
    </div>
  </div>
</template>

<script>
/* eslint-disable */
    export default {
        name: "AddForm",
        data(){
          return{
            brands:null,
            brand:null,
            types:null,
            type:null,
            information:[],
            status:"Solicitando",
            mas:null,
          }
        },
        methods:{
          async getProductInfos(){
            const req = await fetch("http://localhost:3000/productInfos")
            const data=await req.json();

            console.log(data);
            this.brands = data.brands;
            this.types = data.types;
          }
        },
        mounted(){
          this.getProductInfos();
        }
    }
    </script>
            
    <!-- Add "scoped" attribute to limit CSS to this component only -->
    <style scoped>
        @import '../../../css/Styles.scss';
    </style>
            
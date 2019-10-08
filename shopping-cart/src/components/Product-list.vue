<template>
    <div>
        <Product-card class="card" v-for="(product, index) in products" v-bind:product="product"  v-bind:index="index" @update="changeBtn"/>
    </div>
</template>

<script> 
import Vue from "vue";
import ProductCard from './Product-card.vue';

export default {
    name: 'Product-list',
    components : { ProductCard },
    props :  {
        products : Array
    },
    methods: {
    changeBtn(operation, index){
        switch(operation) {
            case 'increment' : {this.products[index].quantity =  this.products[index].quantity + 1; break;}
            case 'decrement' :  {this.products[index].quantity =  this.products[index].quantity - 1; break;}
           
        }
           
        }
    
  } ,
   created: function() {
        this.$parent.$on('update', this.changeBtn);
  }
}
</script>

<style scoped>
  .card{
      border:1px solid #ccc;
      padding: 10px;
      min-height: 150px;
      display: flex;
      margin: 10px 0;
      border-radius: 10px;
      
  }
</style>
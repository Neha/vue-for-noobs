<template>
  <div id="app">
    <h2>Shopping List!!</h2>
    <Product-list v-bind:products="products" />
    <footer>made in VueJS</footer>
  </div>
</template>

<script>
import Vue from "vue"
import ProductList from "./components/Product-list.vue";
import style from './style/style.css';

const products = [
  { name: "icecream", quantity: 10, price: 200 },
  { name: "cake", quantity: 100, price: 550 },
  { name: "shakes", quantity: 410, price: 390 }
];

export default {
  name: "app",
  data: function() {
    return {
     products
    };
  },
  components: {
    ProductList
  }
};
</script>


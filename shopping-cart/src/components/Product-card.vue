<template>
  <div v-bind:index="index" class="cardList">
      <h3>Quantity: {{product.name}}</h4> 
      <h4>Quantity: {{product.quantity}}</h4>
      <h4>Price: {{product.price}}</h4>
      <div class="buttonWrapper">
        <button  @click="() => {change('decrement', index)}" v-bind:value="product.quantity" v-bind:index="index">-</button>
        <button  @click="() => {change('increment', index)}" v-bind:value="product.quantity" v-bind:index="index" >+</button>
      </div>
  </div>
</template>

<script>
import Vue from "vue";

export default {
  name: "Product-card",
  props: ["product", "index"],
  methods: {
    change(operation, index){
     this.$emit('update', operation, index)
    }
  }
};
</script>


<style scoped>
  .cardList{
      flex-direction: column;
  }
  button{
   width: 80px;
   padding: 5px 10px;
  }
  h4{
    margin: 10px 0;
    font-size: 16px;
  }
</style>
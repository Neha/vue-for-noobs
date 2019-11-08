<template>
  <div id="app">
    <h2>VueJS Form</h2>
    <Form-card />
    <footer>made in VueJS</footer>
  </div>
</template>

<script>
import Vue from "vue"
import FormCard from "./components/Form.vue";
import style from './style/style.css';



export default {
  name: "app",
  components: {
    FormCard
  }
};
</script>

<style scoped>
  footer{
    margin-top: 20px;
    color: #000;
  }
</style>


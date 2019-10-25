<template>
  <div id="app">
    <h2>Shopping List!!</h2>
    <FormCard />
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


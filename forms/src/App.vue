<template>
  <div id="app">
    <h2>Same block user data printing</h2>
    <FormCard />
    <h2>Hide the form and display the user data block</h2>
    <FormMessage />
    <footer>made in VueJS</footer>
  </div>
</template>

<script>
import Vue from "vue"
import FormCard from "./components/Form.vue";
import FormMessage from "./components/Form-message.vue";
import style from './style/style.css';

export default {
  name: "app",
   components: {
    FormCard,
    FormMessage
  }
};
</script>


<template>
  <section class="form-wrapper" userData="userData">
    <h3>Thank you for your feedback!!</h3>
    <p class="successMessage">The name is {{ userData.name}} , email is {{ userData.email }}, city is {{ userData.city}} and message is {{ userData.errorMessage}}</p>
  </section>
</template>

<script>
import Vue from 'vue';

export default {
  name: 'User-data',
  props: ['userData']
};
</script>
<style scoped>
h3{
  text-align: center;
  font-size: 20px;
  }

.successMessage {
  margin: 20px 0;
  font-size: 18px;
  text-align: center;
  line-height: 24px;
  color: green;
}
</style>
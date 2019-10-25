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
.form-wrapper {
  width: 80%;
  margin: 0 auto;
  border-radius: 5px;
  border: 1px solid #000;
  box-shadow: 5px 5px 2px #000;
  background: #fff;
  padding: 10px;
}

label {
  font-size: 16px;
  display: block;
  font-weight: 400;
}

input {
  height: 32px;
}

input,
textarea {
  width: 96%;
  padding: 5px;
  border: 1px solid #ccc;
  background: #eee;
}

form > div {
  margin: 20px 0;
}

textarea {
  height: 100px;
}

button {
  width: 80%;
  display: block;
  margin: 10px auto;
  background: rgb(74, 194, 18);
  text-align: center;
  font-size: 30px;
  color: #fff;
  padding: 10px 0;
}

.errorMessage {
  color: red;
  text-align: center;
}

.successMessage {
  font-size: 19px;
  text-align: center;
  line-height: 21px;
  color: green;
}
</style>
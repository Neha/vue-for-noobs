<template>
  <section class="form-wrapper" v-if="isForm == false">
    <p v-if="isSubmitted === false" class="errorMessage">{{ errorMessage }}</p>
    <form type="submit">
      <div>
        <label>Full Name</label>
        <input type="text" v-model="userData.name" />
      </div>
      <div>
        <label>email</label>
        <input type="email" v-model="userData.email" />
      </div>
      <div>
        <label>City</label>
        <input type="text" v-model="userData.city" />
      </div>

      <div>
        <label>Message</label>
        <textarea v-model="userData.message" />
      </div>
      <button @click.prevent="submitted">Submit</button>
      </form>
     </section>
     <section  v-else>
      <User-data v-bind:userData="userData"/>
     </section>
</template>


<script>
import Vue from 'vue';
import UserData from './User-data.vue';

export default {
  name: 'Form-message',
  data() {
    return {
      userData: {
        name: '',
        email: '',
        city: '',
        message: ''
      },
      isSubmitted: '',
      errorMessage: '',
      isForm: false
    };
  },
  components: {
      UserData
  },
  methods: {
    submitted(e) {
      e.preventDefault();
      if (
        this.userData.name !== '' &&
        this.userData.email !== '' &&
        this.userData.city !== ''
      ) {
        this.isSubmitted = true;
        this.isForm = true;
        this.message = 'Form is filled';
      } else {
        this.errorMessage = 'oh!! please fill the form';
        this.isSubmitted = false;
      }
    }
  }
};
</script>
<style scoped>
label{
    font-size:16px;
    display: block;
    font-weight: 400;
  }

  input{
    height: 32px;

  }

  input, textarea{
    width: 96%;
    padding: 5px;
    border: 1px solid #ccc;
    background: #eee;
  }

  form > div{
    margin: 20px 0
  }

  textarea{
    height: 100px;
  }

  button{
    width: 80%;
    display: block;
    margin: 10px auto;
    background: rgb(74, 194, 18);
    text-align: center;
    font-size: 30px;
    color: #fff;
    padding: 10px 0;
  }

  .errorMessage{
    color: red;
    text-align: center;
  }

 .successMessage{
    font-size: 19px;
    text-align: center;
    line-height: 21px;
    color:green;
  }
</style>
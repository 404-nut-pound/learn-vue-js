<template>
  <!-- .prevent modifier를 사용하면 event.preventDefault() 기본 적용 -->
  <form v-on:submit.prevent="submitForm">
    <div>
      <label for="username">ID: </label>
      <input type="text" id="username" v-model="username" />
    </div>
    <div>
      <label for="password">PW: </label>
      <input type="password" id="password" v-model="password" />
    </div>
    <button type="submit">LOGIN</button>
  </form>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      username: '',
      password: '',
    };
  },
  methods: {
    submitForm: function () {
      console.log(this.username, this.password);

      let url = 'https://jsonplaceholder.typicode.com/users';
      let data = {
        username: this.username,
        password: this.password,
      };

      axios
        .post(url, data)
        .then((response) => console.log(response))
        .catch((error) => console.log(error));
    },
  },
};
</script>

<style>
</style>
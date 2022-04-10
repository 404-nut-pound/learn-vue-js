<template>
  <form v-on:submit="submitForm">
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
export default {
  data() {
    return {
      username: '',
      password: '',
    };
  },
  methods: {
    submitForm: function (event) {
      event.preventDefault();

      console.log(this.username, this.password);
    },
  },
};
</script>

<style>
</style>
<template>
  <div>
    {{ message }}
    <app-header
      v-bind:appHeaderProps="header"
      v-on:renew="renewMessage"
    ></app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

export default {
  data() {
    return {
      message: 'Hello, CLI!!!',
      header: 'Header!!!',
    };
  },
  components: {
    'app-header': AppHeader,
  },
  methods: {
    renewMessage: function () {
      this.message = 'from AppHeader';
    },
  },
};
</script>

<style>
</style>
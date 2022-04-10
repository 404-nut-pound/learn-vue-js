<template>
  <header>
    <h1>{{ appHeaderProps }}</h1>
    <button v-on:click="sendEvent">send emit</button>
  </header>
</template>

<script>
export default {
  props: ['appHeaderProps'],
  methods: {
    sendEvent: function () {
      this.$emit('renew');
    },
  },
};
</script>

<style>
</style>
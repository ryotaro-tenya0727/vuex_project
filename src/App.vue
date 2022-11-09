<template>
  <div id="app">
    <p><button v-on:click="increment">UP</button></p>
    <h1>Count:{{ count }}</h1>
  </div>
</template>

<script>
export default {
  name: 'app',
  methods: {
    increment: function () {
      this.$store.dispatch('incrementOne');
    },
  },
  computed: {
    count: function () {
      return this.$store.state.count;
    },
  },
};
</script>

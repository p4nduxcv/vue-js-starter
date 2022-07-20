<template>
  <h1>HELLO {{ name }}</h1>
  <div v-html="channel"></div>
  <div v-html="hack"></div>
  <div v-bind:id="headingId">Heading</div>
  <button v-bind:id="headingId">Button</button>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      name: "PANDULA DAN",
      channel: "<b>Mastach</b>",
      hack: `<a href='#' onclick="alert('You Have Been HAcked')">CLIKC<a/>`,
      headingId: "heading",
      isDisabled: true,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
